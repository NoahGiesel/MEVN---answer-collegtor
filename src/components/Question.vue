<template>
  <div class="question"> 
    <form action=""> 
      <h2>Answear my questions...</h2>
      <h3>How much is <span>2+2</span> ?</h3>
      <input type="radio" name="gender" id="male" value="male"> 
      <label for="male">Male</label>
      <br>
      <input type="radio" name="gender" id="female" value="female"> 
      <label for="female">Female</label>
      <br>
      <input type="radio" name="gender" id="Other" value="Other"> 
      <label for="other">Other</label>
       <br>
      <button v-on:click="check">Submit</button> 
    
    </form>
  </div>
</template>

<script>
export default {
  name: 'Question',
  
  methods : {
     check: function ( e ) { 
       e.preventDefault(); 
       var answerArray = [];
       let counter = 0;
       const answer1 = document.getElementById("male") ;
       const answer2 = document.getElementById("female") ;
       const answer3 = document.getElementById("Other") ;

      if(answer1.checked ) {
        answerArray.push(counter,answer1.value);  
        console.log(answerArray)
        counter++
      }
      if(answer2.checked ) {  
        answerArray.push(counter,answer2.value);  
        console.log(answerArray)
        counter++      
        }
      if(answer3.checked ) {  
        answerArray.push(counter,answer3.value);  
        console.log(answerArray)
        counter++      
        }

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
