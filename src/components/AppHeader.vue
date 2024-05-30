<script>
export default {
  data() {
    return {
        links: [
            {
                text: "Donna",
                url : "https://www.google.com",
                
            },
            {
                text: "Uomo",
                url : "https://www.google.com",
               
            },
            {
                text: "Bambini",
                url : "https://www.google.com",
               
            },
          
        ],
       
    };
    
    }
}

</script>
<template>
    <header>
        <div class="header-container">


            <div class="header-links">

                 <ul>
                    <a href=""><li v-for="link in links" v-bind:key="link.text">{{ link.text }}</li></a>
                </ul>
            </div>
        
               
          
            <div class="header-logo">

                <img src="../assets/img/boolean-logo.png" alt="logo">
            </div>
            <div class="header-icons">
                <i class="fa-regular fa-user"></i>
                <i class="fa-regular fa-heart"></i>
                <i class="fa-solid fa-bag-shopping"></i>
            </div>



        </div>

    </header>

</template>

<style scoped>

</style>

