<template>
  <div class="question"> 
    <form action=""> 
      <h2>Answear my questions...</h2>
      <h3>How much is <span>2+2</span> ?</h3>
      <input type="radio" name="gender" id="first" value="first"> 
      <label for="male">3</label>
      <br>
      <input type="radio" name="gender" id="second" value="second"> 
      <label for="female">4</label>
      <br>
      <input type="radio" name="gender" id="third" value="third"> 
      <label for="other">1</label>
       <br>
      <button v-on:click="check">Submit</button> 
    
    </form>
  </div>
</template>

<script>
export default {
  name: 'Question',
  
  data :  function() {
      return {
         answerArray:  []
      };
  },
  
  methods : {
     check: function ( e ) { 
       e.preventDefault(); 
       const answer1 = document.getElementById("first") ;
       const answer2 = document.getElementById("second") ;
       const answer3 = document.getElementById("third") ;

      if(answer1.checked ) {
        this.answerArray.push( answer1.value)  
      }
      if(answer2.checked ) {  
        this.answerArray.push(answer2.value) 
        }
      if(answer3.checked ) {  
        this.answerArray.push(answer3.value) 
        } 
       console.log(this.answerArray);
       
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>  

  .question {
    position: absolute ;
    left: 50% ;
    top: 50% ; 
    transform: translate(-50%,-50%) ;
  }

  span {
    font-weight: bold ;
    color: blue ;
  }
 


</style>
