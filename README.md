<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap 4 Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js"></script>
<script>
// Set the date we're counting down to
var countDownDate = new Date("December 31, 2018 16:00:00").getTime();

// Update the count down every 1 second
var x = setInterval(function() {

  // Get todays date and time
  var now = new Date().getTime();

  // Find the distance between now and the count down date
  var distance = countDownDate - now;

  // Time calculations for days, hours, minutes and seconds
  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);

  // Display the result in the element with id="demo"
 document.getElementById("days").innerHTML = days + " days";

document.getElementById("hours").innerHTML = hours + " hours";

document.getElementById("minutes").innerHTML = minutes + " minutes";

document.getElementById("seconds").innerHTML = seconds + " seconds";

  // If the count down is finished, write some text 
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("days").innerHTML = "EXPIRED";
  }
}, 1000);
</script>

<style>

body{
background-color : #009688;

}

</style>
</head>
<body>

<!-- Display the countdown timer in an element -->
<p id="demo"></p>

<center>

<div class="card" style="width: 18rem;">

  <div id="days" class="card-body">
    
  </div>
  </div>
  <br>
  <br>
  
  <div class="card" style="width: 18rem;">
  <div id="hours" class="card-body">
    
  </div>
  </div>
  <br>
  <br>
  <div class="card" style="width: 18rem;">
  <div id="minutes" class="card-body">
    
  </div>
  </div>
  <br>
  <br>
  <div class="card" style="width: 18rem;">
  <div id="seconds" class="card-body">
    
  </div>
  </div>
  


</center>



</body>
</html> 
