<script setup>
import axios from "axios"
</script>

<template>
<div class="container p-5">
    <table id="mainTable">
        <thead>
            <tr>
                <th>BP Code</th>
                <th>Primary Cab</th>
                <th>Age</th>
                <th>City</th>
                <th>County</th>
                <th>VPA?</th>
                <th>BBC</th>
            </tr>
        </thead>
        <tbody v-for="(data,index) in bpData" v-bind:key="index">
            <tr @click="openPopup">
                <td>{{ data.BroadwayCode }}</td>
                <td>{{ data.PRIMARYCAB }}</td>
                <td>{{ data.SEQUENCE }}</td>
                <td>{{ data.BroadwayCode }}</td>
                <td>{{ data.County }}</td>
                <td>{{ data.VPA }}</td>
                <td>{{ data.BBC }}</td>
            </tr>
        </tbody>
    </table>
</div>
</template>



<script>
export default{
    data() {
        return {
            bpData:[],
            loggedIn: false
        };
    },
    components() {
        LoginPage,
        LandPage,
        FontAwesomeIcon;
    },
    mounted() {
      axios.get("./Data/data.json")
      .then(response => (this.bpData = response.data))
    },
    methods: {
        openPopup: function () {
          alert('ok')
        }
      }
}
</script>
