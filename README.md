# Double-slider
Double Slider using Jquery


<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
	<!-- Latest compiled and minified JavaScript -->
  <script src="https://code.jquery.com/jquery-2.1.3.min.js"></script>
  <script src="http://code.jquery.com/ui/1.11.1/jquery-ui.min.js"></script>
  <link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
  <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>
</head>
<body>
 <div class="container" style="margin-top:60px;">
 <div class="row">
 <div class="col-md-6">
 <p>
 <label for="amount1"style="font-size:15px;text-align:center;font-weight:700; ">Price range : </label>
 <input type="text" id="amount1" readonly style="border:0; color:#f06225; font-weight:bold;font-family: Open sans; font-weight:bold;width:100px;"></p>
<div id="slider1"></div>
</div>
</div>
</div>
 <script>
$( function() {
    $( "#slider1" ).slider({
      range: true,
      min: 0,
      max: 500,
      values: [ 75, 300 ],
      slide: function( event, ui ) {
        $( "#amount1" ).val( "$" + ui.values[ 0 ] + " - $" + ui.values[ 1 ] );
      }
    });
    $( "#amount1" ).val( "$" + $( "#slider1" ).slider( "values", 0 ) +
      " - $" + $( "#slider1" ).slider( "values", 1 ) );
  } );
</script>
</body>
</html>
