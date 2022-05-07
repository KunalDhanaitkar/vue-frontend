<template>

    <div class="container">
        
        <div>      
            <img class="image" :src="resource.image" />
        </div>

        <div id="item-header">
            <font size="4"><b><u>{{resource.title}}</u></b></font>, {{resource.year}}
        </div>

        <div id="item-description">
            {{resource.description}}
        </div>

        <div id="item-type">
            Type - <b>{{resource.type}}</b>
        </div>

        <div id="item-link">
        
            <a class="down-link" :href="resource.link" :target="_blank">
                <button class="btn"><u>Learn More..</u></button>
            </a>

        </div>

    </div>
    
</template>

<script>

export default {
    name: 'ResourceItem',
    props:{
        resource: Array
    }
}
</script>

<style scoped>

.container{
    background-color: rgb(252, 178, 69);
    color:black;
    padding: 1em;
    border-radius: 15px;
    
    box-shadow: 0px 0px 2px 2px white;
    transition: 1s;
    width: 280px;
    height: 580px;
    overflow: hidden;
}

.image{
    height: 300px;
    width: 220px;
    margin: 8px
}

#item-header{
    text-align: center;
    text-emphasis: bold;
    font-size: larger;
}

.btn {
  color: rgba(0, 0, 0, 0.87);
  background-color: #ffd694;
  box-shadow: 0 3px 1px -2px rgb(0 0 0 / 20%), 0 2px 2px 0 rgb(0 0 0 / 14%),
    0 1px 5px 0 rgb(0 0 0 / 12%);
  box-sizing: border-box;
  position: relative;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  cursor: pointer;
  outline: none;
  border: none;
  -webkit-tap-highlight-color: transparent;
  display: inline-block;
  white-space: nowrap;
  text-decoration: none;
  vertical-align: baseline;
  text-align: center;
  margin: 0;
  min-width: 64px;
  line-height: 36px;
  padding: 6px 16px;
  border-radius: 4px;
  overflow: visible;
  transform: translate3d(0, 0, 0);
  transition: 400ms cubic-bezier(0.25, 0.8, 0.25, 1),
    box-shadow 280ms cubic-bezier(0.4, 0, 0.2, 1);
  width: 100%;
  
}

#item-description{
    text-align: center;
    font-size: large;
}

#item-type{
    text-align: center;
    padding-bottom: 2px;
}

</style>