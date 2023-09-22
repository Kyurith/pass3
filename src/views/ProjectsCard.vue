<template>
    <div class="main-container">
        <div class="project-card" v-for="(items, index) in projectData.ProjectsArray" v-bind.key="items">
            <h2>{{projectData.ProjectsArray[index].Title}}</h2>
            <img :src="projectData.ProjectsArray[index].Image" alt="" width="500"/>
            <p>{{projectData.ProjectsArray[index].About}}</p>
            <a href="https://github.com">
                <img src="../assets/github.png" alt="" width="30"/>
             </a>
</div>
    </div>
</template>

<script>
    import jsonData from "/projects.json"
export default {
    data(){
        return{
            projectData: jsonData
        }
    }
}
</script>

<style >
    @import "./src/components/projectcards.css";
</style>
