<script setup>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import LoginPage from './components/LoginPage.vue'
import LandPage from './components/LandPage.vue'
import axios from "axios"
import DataTable from "./components/DataTable.vue"
</script>

<template >


<ul class="nav nav-tabs" id="navId">
    <li class="nav-item">
        <a href="#tab1Id" class="nav-link active">Active</a>
    </li>
    <li class="nav-item dropdown">
        <a class="nav-link dropdown-toggle" data-toggle="dropdown" href="#" role="button" aria-haspopup="true" aria-expanded="false">Dropdown</a>
        <div class="dropdown-menu">
            <a class="dropdown-item" href="#tab2Id">Action</a>
            <a class="dropdown-item" href="#tab3Id">Another action</a>
            <div class="dropdown-divider"></div>
            <a class="dropdown-item" href="#tab4Id">Action</a>
        </div>
    </li>
    <li class="nav-item">
        <a href="#tab5Id" class="nav-link">Another link</a>
    </li>
    <li class="nav-item">
        <a href="#" class="nav-link disabled">Disabled</a>
    </li>
</ul>

<!-- Tab panes -->
<div class="tab-content">
    <div class="tab-pane fade show active" id="tab1Id" role="tabpanel"></div>
    <div class="tab-pane fade" id="tab2Id" role="tabpanel"></div>
    <div class="tab-pane fade" id="tab3Id" role="tabpanel"></div>
    <div class="tab-pane fade" id="tab4Id" role="tabpanel"></div>
    <div class="tab-pane fade" id="tab5Id" role="tabpanel"></div>
</div>
<div id="mainDiv" class="container p-5">
  <LandPage/>

  <DataTable/>
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
    }
}
</script>


