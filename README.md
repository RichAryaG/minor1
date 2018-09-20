<!DOCTYPE html>
<html lang="en">
<head>
<title>Syslog Management</title>

<!-- CSS -->
<style>
.myForm {
font-family: "Lucida Sans Unicode", "Lucida Grande", sans-serif;
font-size: 0.8em;
width: 20em;
padding: 1em;
border: 1px solid #ccc;
}

.myForm * {
box-sizing: border-box;
}

.myForm fieldset {
border: none;
padding: 0;
}

.myForm legend,
.myForm label {
padding: 0;
font-weight: bold;
}

.myForm label.choice {
font-size: 0.9em;
font-weight: normal;
}

.myForm input[type="text"],
.myForm input[type="tel"],
.myForm input[type="email"],
.myForm input[type="datetime-local"],
.myForm select,
.myForm textarea {
display: block;
width: 100%;
border: 1px solid #ccc;
font-family: "Lucida Sans Unicode", "Lucida Grande", sans-serif;
font-size: 0.9em;
padding: 0.3em;
}

.myForm textarea {
height: 100px;
}

.myForm button {
padding: 1em;
border-radius: 0.5em;
background: #eee;
border: none;
font-weight: bold;
margin-top: 1em;
}

.myForm button:hover {
background: #ccc;
cursor: pointer;
}
</style>

</head>
<body>

<form class="myForm" method="get" enctype="application/x-www-form-urlencoded" action="/html/codes/html_form_handler.cfm">

<p>
<label>Host Name
<input type="text" name="host_name" required>
</label> 
</p>

<p>
<label>Choose your Virtual machine
<select id="virtual_machine" name="virtual_machine">
<option value="" selected="selected">Select One</option>
<option value="ubuntu" >ubuntu</option>
<option value="CentOS" >CentOS</option>
<option value="RedHat_linux" >RedHat linux</option>
<option value="windows" >Microsoft Windows</option>
</select>
</label> 
</p>



<p>
<label>TimeSlot
<input type="datetime-local" name="timeslot">
</label>
</p>



<p>		
<label>Email 
<input type="email" name="email_address">
</label>
</p>

<fieldset>
<legend>what info do you require?</legend>
<p><label class="choice"> <input type="radio" name="vm" required value="time"> Uptime </label></p>
<p><label class="choice"> <input type="radio" name="vm" required value="time2"> Downtime </label></p>
<p><label class="choice"> <input type="radio" name="vm" required value="time3"> seektime </label></p>
<p><label class="choice"> <input type="radio" name="vm" required value="count1"> number of errors </label></p>
<p><label class="choice"> <input type="radio" name="vm" required value="count2"> number of times system was started </label></p>
<p><label class="choice"> <input type="radio" name="vm" required value="vmname"> most freuently used VM </label></p>
</fieldset>

<fieldset>
<legend>multiple info needed?</legend>
<p><label class="choice"> <input type="checkbox" name="info" value="time">  Uptime  </label></p>
<p><label class="choice"> <input type="checkbox" name="info" value="time2"> Downtime </label></p>
<p><label class="choice"> <input type="checkbox" name="info" value="time3"> seektime </label></p>
</fieldset>





<p>
<label>any more improvements?
<textarea name="comments" maxlength="500"></textarea>
</label>
</p>

<p><button>Start</button></p>

</form>

</body>
</html>
