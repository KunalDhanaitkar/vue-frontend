<template>
    <div class="contact">
            <div class="card-title" style="color:white;">For More Information, Contact Us</div>

                    <div class="flex-container">
                    
                    
                    <div class="phone">
                        <a href=""
                          target="_blank">
                          <i class="fa-solid fa-phone"></i>
                        </a>
                    </div>

                    <div class="mail">
                        <a href=""
                          target="_blank">
                          <i class="fa-solid fa-envelope"></i>
                        </a> 
                    </div>

                    <div class="telegram">
                        <a href=""
                          target="_blank">
                          <i class="fa-brands fa-telegram"></i>
                        </a>
                    </div>

                    <div class="facebook">
                        <a href=""
                          target="_blank">
                          <i class="fa-brands fa-facebook"></i>
                        </a>
                    </div>

                    </div>
    </div>

</template>

<script>

export default {
  name: "AppFooter",
  setup() {
    return {};
  },
};
</script>

<style>

.contact{
    overflow: auto;
    border: 0.3em solid black;
    padding: 10px;
    border-radius: 5px;
    background-color: rgb(252, 178, 69);
}

.card-title{
    text-align: center;
    font-size: x-large;
    font-weight: bolder;
    text-decoration: underline;
    padding-bottom: 20px;
}

.flex-container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}
.phone {
  font-size: 35px;
  text-align: center;
  text-decoration: none;
}
.mail {
  font-size: 35px;
  text-align: center;
  text-decoration: none;
}
.telegram {
  font-size: 35px;
  text-align: center;
  text-decoration: none;
}
.facebook {
  font-size: 35px;
  text-align: center;
  text-decoration: none;
}

</style>
