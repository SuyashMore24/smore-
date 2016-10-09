# smore-
Leave management system
<html>

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />

   <link rel="stylesheet" href="../styles.css">
   <script src="http://code.jquery.com/jquery-latest.min.js" type="text/javascript"></script>
   <script src="script.js"></script>
   <script type="text/javascript" src='jquery.min.js'></script>
<style type="text/css">
input{background:#FFE4B5; size:10px; border-radius:5px; }
table{font-size:16px; font-weight:bold; border-collapse:collapse; }
select{background:#98FB98; width:150px; height:30px; font-size:12px; font-weight:bold;}
option{background:#7CCD7C; font-weight:bold; font-size:12px; }
table th{font-size:18px; font-weight:bold; background:#006400; color:white; }
</style>

<?php
session_start();
$con = mysql_connect("localhost","Staff","9821150615");
mysql_select_db("RMCET", $con);
				?>


<body >

<table align="center" cellpadding="0"  width="800" border="0">
  <tr>
    <td><br/><br/><h1 align="center" class="heading">"Welcome to Admin Panel"</h1>
      <p align="center">&nbsp;</p>
      <table width="638" border="0" align="center">
        <tr>
          <td width="107"><a href="insert.php"><img border="0" name="test
     " src="images/cooltext457947887.png" onmouseover="this.src='images/cooltext457947887MouseOver.png';" onmouseout="this.src='images/cooltext457947887.png';" /></a></td>
          <td width="515" class="options">To add new Staff</td>
        </tr>
		        <tr>
          <td width="107"><a href="insertstud.php"><img border="0" name="test
     " src="images/cooltext457947887.png" onmouseover="this.src='images/cooltext457947887MouseOver.png';" onmouseout="this.src='images/cooltext457947887.png';" /></a></td>
          <td width="515" class="options">To add new student</td>
        </tr>

        <tr>
          <td><a href="delete.php"><img border="0" src="images/cooltext457947999.png" onmouseover="this.src='images/cooltext457947999MouseOver.png';" onmouseout="this.src='images/cooltext457947999.png';" /></a></td>
          <td class="options">To delete records</td>
        </tr>
        <tr>
          <td><a href="modify.php"><img border="0" src="images/cooltext457948094.png" onmouseover="this.src='images/cooltext457948094MouseOver.png';" onmouseout="this.src='images/cooltext457948094.png';" /></a></td>
          <td class="options">to modify a student records</td>
        </tr>
      </table>
      <p align="center"><a href="../about.php"><img src="images/cooltext457954859.png" alt="" border="0" onmouseover="this.src='images/cooltext457954859MouseOver.png';" onmouseout="this.src='images/cooltext457954859.png';" /></a><a href="../"><img border="0" src="images/cooltext457951462.png" alt="Go Back" onmouseover="this.src='images/cooltext457951462MouseOver.png';" onmouseout="this.src='images/cooltext457951462.png';" /></a><a href="http://www.ahmadmushtaq.com"><img src="images/cooltext457955210.png" alt="" border="0" onmouseover="this.src='images/cooltext457955210MouseOver.png';" onmouseout="this.src='images/cooltext457955210.png';" /></a></p>
  </tr>
</table>
<h1 align="center" class="heading">&nbsp;</h1>
</body>
</html>
<div width="300px" float="left">
          <a href="insert.php"><img border="0" name="test
     " src="images/cooltext457947887.png" onmouseover="this.src='images/cooltext457947887MouseOver.png';" onmouseout="this.src='images/cooltext457947887.png';" /></a>Staff
	         <a href="insertstud.php"><img border="0" name="test
     " src="images/cooltext457947887.png" onmouseover="this.src='images/cooltext457947887MouseOver.png';" onmouseout="this.src='images/cooltext457947887.png';" /></a>Stundet

     <a href="delete.php"><img border="0" src="images/cooltext457947999.png" onmouseover="this.src='images/cooltext457947999MouseOver.png';" onmouseout="this.src='images/cooltext457947999.png';" /></a>
        
       <a href="modify.php"><img border="0" src="images/cooltext457948094.png" onmouseover="this.src='images/cooltext457948094MouseOver.png';" onmouseout="this.src='images/cooltext457948094.png';" /></a>
	   <br/><br/>

</div>
<div>
<form method="post" action="Stregistration.php" onsubmit="return staff();"  name="staffres" enctype="multipart/form-data">
        <table align="center" width="500px" border="1px" height="300px" >

             <tr>
               <td width="129" colspan="2"><center><strong>Add New Staff Data</strong></center></td>
            </tr>

          <tr>
               <td width="129"><center><strong>First Name</strong></center></td>
               <td><center><input type="text" name="Fname" id="textfield" />
              </center> </td>
          </tr>

          <tr>
            <td><center><strong>Midddle name:</strong></center></td>
            <td><center><input type="text" name="Mname" id="textfield2" /></center></td>
          </tr>

           <tr>
               <td width="129"><center><strong>Last Name</strong><center></td>
               <td><center><input type="text" name='Lname' id="textfield" />
             </center>  </td>
          </tr>

          <tr>
            <td><center><strong>Staff id:</strong></center></td>
            <td><center><input type="text" name='Stusername' id="textfield3" /></center></td>
          </tr>
           
		   <tr>
            <td><center><strong>Password</strong></center></td>
            <td><center><input type="text" name='Stpassword' id="textfield3" /><center></td>
           </tr> 

          <tr>
<td><b>Branch</b></td>
<td><center><select name='Branch' onblur="staff()" id="j">
<option>COMP</option>
<option>MECH</option>
<option>AUTO</option>
<option>EXTC</option>
</select><div id="dep"></center></div>          </tr>
		  <tr>
<td><b>Year</b></td>
<td><center><select name='Year' onblur="staff()" id="j">
<option>S.E</option>
<option>T.E</option>
<option>B.E</option>
</select><div id="dep"></center></div> </tr>
        </table>
        <p align="center"><center>
          <label>
            <input type="submit" name="button" id="button" value="Submit" />
          </center></label>
        </p>
        <p align="center"><a href="insert.php"><img border="0" src="images/cooltext457951462.png" alt="Go Back" onmouseover="this.src='images/cooltext457951462MouseOver.png';" onmouseout="this.src='images/cooltext457951462.png';" /></a></p>
      </form>
  </tr>
</table>
<h1 align="center" class="heading">&nbsp;</h1>
</div>
</body>
</html>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Control Panel :: Student Information Panel:: Institute of Information Technology, BZU</title>
<style type="text/css">
<!--
.heading {
	color: #F90;
	font-family: "Comic Sans MS", cursive;
}
.options {
	font-family: "Comic Sans MS", cursive;
	font-size: 16px;
	font-style: oblique;
	color: #F93;
}
-->
</style>
</head>

<body background="images/1019286_abstract_orange_tiles_background_.jpg">

<br />
<br />
<br />
<table align="center" cellpadding="0" bgcolor="#FFFFFF" width="800" border="0">
  <tr>
    <td><h1 align="center" class="heading"><img src="images/cooltext457948700.png" width="747" height="58" alt="Welcome to Admin Panel" /></h1>
  <p align="center">
    <?php 
	 $sname=$_REQUEST['name']; 
	 $roll=$_REQUEST['rollno'];
	 $reg=$_REQUEST['reg'];
	 $dept=$_REQUEST['dept']; 
	 
	 $link=mysql_connect("localhost","root","") or die("Cannot Connect to the database!");
	
	 mysql_select_db("department",$link) or die ("Cannot select the database!");
	 $query="INSERT INTO students (sname, rollno, regno, dname) values('".$sname."', '".$roll."', '".$reg."', '".$dept."')";
		
		  if(!mysql_query($query,$link))
		  {die ("An unexpected error occured while saving the record, Please try again!");}
		  else
		 {
		  echo "New record saved successfully!";}
	 ?>

      </p>
      <p align="center"><img onclick="javascript: history.go(-1)" src="images/cooltext457951462.png" onmouseover="this.src='images/cooltext457951462MouseOver.png';" onmouseout="this.src='images/cooltext457951462.png';" /><a href="../"><img border="0" src="images/cooltext457951615.png" onmouseover="this.src='images/cooltext457951615MouseOver.png';" onmouseout="this.src='images/cooltext457951615.png';" /></a></p>
      <p align="left">&nbsp;</p>
    <p align="left">&nbsp;</p></td>
  </tr>
</table>
<h1 align="center" class="heading">&nbsp;</h1>
</body>
</html>

<div width="300px" float="left" height="400px">
          <a href="insert.php"><img border="0" name="test
     " src="images/cooltext457947887.png" onmouseover="this.src='images/cooltext457947887MouseOver.png';" onmouseout="this.src='images/cooltext457947887.png';" /></a>
     <a href="delete.php"><img border="0" src="images/cooltext457947999.png" onmouseover="this.src='images/cooltext457947999MouseOver.png';" onmouseout="this.src='images/cooltext457947999.png';" /></a>
        
       <a href="modify.php"><img border="0" src="images/cooltext457948094.png" onmouseover="this.src='images/cooltext457948094MouseOver.png';" onmouseout="this.src='images/cooltext457948094.png';" /></a>

</div>
<div>
<center>
<Form method=post onsubmit="validate()" name="registration" action="../Registration.php">
<table height="500px" width="500px" border="1">
<tr>
<td colspan="2"><b><center>Add new data</b></center></td>
</tr>
<tr>
<td><b>Student id:</b></td>
<td><input type=text name='id'>
</tr>
<tr>
<td><b>First name:</b></td>
<td><input type=text name='Fname' onblur="validate()"><div id="error"></div></td>
</tr>
<tr>
<td><b>Middle name:</b></td>
<td><input type=text name='Mname'><div id="error"></div></td>
</tr>
<tr>
<td><b>Last name:</b></td>
<td><input type=text name='Lname'><div id="error"></div></td>
</tr>
<tr>
<td><b>Username</b></td>
<td><input type="username" name='username'><div id="error"></div></td>
</tr>
<td><b>Password:</b></td>
<td><input type="password" name='password'><div id="error"></div></td>
<tr>
</tr>
<tr>
<td><b>Email ID:</b></td>
<td><input type=text name='email'><div id="error"></div></td>
</tr>
<tr>
<td><b>Address:</b></td>
<td><textarea rows="4" cols="21"  name='Address'></textarea><div id="error"></div></td>
</tr>
<tr>
<td><b>Birthdate:</b></td>
<td><input type=text name='Birthdate'><div id="error"></div></td>
</tr>
<tr>
<td><b>Mobile number:</b></td>
<td><input type=text name='Mnumber'><div id="error"></div></td>
</tr>
<tr>
<td><b>Year:</b></td>
<td><select name='Year'>
<option>S.E</option>
<option>T.E</option>
<option>B.E</option>
</select>
</td>
<div id="error"></div>
</tr>

<tr>
<td><b>Department:</b></td>
<td><select name='Department'>
<option>COMP</option>
<option>MECH</option>
<option>AUTO</option>
<option>EXTC</option>
</select>
</td><div id="error"></div>
</tr>

<tr>
<td colspan="2"><center><input type=submit value="submit" Onsubmit="validate()";></center></td>
</tr>
</form>
</table>
<center>
<h1 align="center" class="heading">&nbsp;</h1>
</div>
</body>
</html>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Control Panel :: Student Information Panel:: Institute of Information Technology, BZU</title>
<style type="text/css">
<!--
.heading {
	color: #F90;
	font-family: "Comic Sans MS", cursive;
}
.options {
	font-family: "Comic Sans MS", cursive;
	font-size: 16px;
	font-style: oblique;
	color: #F93;
}
-->
</style>
</head>

<body background="images/1019286_abstract_orange_tiles_background_.jpg">

<br />
<br />
<br />
<table align="center" cellpadding="0" bgcolor="#FFFFFF" width="800" border="0">
  <tr>
    <td><h1 align="center" class="heading"><img src="images/cooltext457948700.png" width="747" height="58" alt="Welcome to Admin Panel" /></h1>
  <p align="center">
    <?php 
	 $sname=$_REQUEST['name']; 
	 $roll=$_REQUEST['rollno'];
	 $reg=$_REQUEST['reg'];
	 $dept=$_REQUEST['dept']; 
	 
	 $link=mysql_connect("localhost","root","") or die("Cannot Connect to the database!");
	
	 mysql_select_db("department",$link) or die ("Cannot select the database!");
	 $query="INSERT INTO students (sname, rollno, regno, dname) values('".$sname."', '".$roll."', '".$reg."', '".$dept."')";
		
		  if(!mysql_query($query,$link))
		  {die ("An unexpected error occured while saving the record, Please try again!");}
		  else
		 {
		  echo "New record saved successfully!";}
	 ?>

      </p>
      <p align="center"><img onclick="javascript: history.go(-1)" src="images/cooltext457951462.png" onmouseover="this.src='images/cooltext457951462MouseOver.png';" onmouseout="this.src='images/cooltext457951462.png';" /><a href="../"><img border="0" src="images/cooltext457951615.png" onmouseover="this.src='images/cooltext457951615MouseOver.png';" onmouseout="this.src='images/cooltext457951615.png';" /></a></p>
      <p align="left">&nbsp;</p>
    <p align="left">&nbsp;</p></td>
  </tr>
</table>
<h1 align="center" class="heading">&nbsp;</h1>
</body>
</html>
<?php
	
	$_SESSION=array();
	
	if(isset($_COOKIE[session_name()]))
	{
		setcookie(session_name(),"",time()-4200,"/");
		
	}
	session_destroy();
	header("Location: ../index.php");
?>

<html>
<head>
   <link rel="stylesheet" href="styles.css">
</head>
<title>RMCET DEPARTMENT</title>
</head>
<body>

<table align="center" cellpadding="0"  width="600" border="0">
  <tr>
    <td><br/><br/><h1 align="center" class="heading">"Welcome to Admin Panel"</h1>
      <p align="center">&nbsp;</p>
	  <div>
          <a href="insert.php"><img border="0" name="test
     " src="images/cooltext457947887.png" onmouseover="this.src='images/cooltext457947887MouseOver.png';" onmouseout="this.src='images/cooltext457947887.png';" /></a>
     <a href="delete.php"><img border="0" src="images/cooltext457947999.png" onmouseover="this.src='images/cooltext457947999MouseOver.png';" onmouseout="this.src='images/cooltext457947999.png';" /></a>
        
       <a href="modify.php"><img border="0" src="images/cooltext457948094.png" onmouseover="this.src='images/cooltext457948094MouseOver.png';" onmouseout="this.src='images/cooltext457948094.png';" /></a>

<div>
    <?php 
	 	 $link=mysql_connect("localhost","root","") or die("Cannot Connect to the database!");
	
	 mysql_select_db("RMCET",$link) or die ("Cannot select the database!");
	 $query="SELECT * FROM student";
		
		  $resource=mysql_query($query,$link);
		  echo "
		<table align=\"center\" border=\"0\" width=\"70%\">
		<tr>
		<td><b>firstName</b></td>
		<td><b>middleName</b></td>
		<td><b>lastName</b></td>
		<td><b>username</b></td>
		<td><b>password</b></td>
		<td><b>emailId</b></td>
		<td><b>Address</b></td>
		<td><b>Birthdate</b></td>
		<td><b>mobileNo</b></td>
		<td><b>Year</b></td>
		<td><b>Department</b></td>
		<td><b>Action</b></td>    
		</tr> ";
while($result=mysql_fetch_array($resource))
	{ 
	echo "<tr><td>".$result[1]."</td><td>".$result[2]."</td><td>".$result[3]."</td><td>".$result[4]."</td><td>".$result[5]."</td><td>".$result[6]."</td><td>".$result[7]."</td><td>".$result[8]."</td><td>".$result[9]."</td><td>".$result[10]."</td><td>".$result[10]."</td><td>
	<a href=\"modify2.php?id=".$result[0]."\"><img border=\"0\" src=\"images/cooltext457953689.png\"/></a>
	</td></tr>";
	} echo "</table>";
	 ?>

        <p align="center"><a href="insert.php"><img border="0" src="images/cooltext457951462.png" alt="Go Back" onmouseover="this.src='images/cooltext457951462MouseOver.png';" onmouseout="this.src='images/cooltext457951462.png';" /></a></p>
  </tr>
</table>
<h1 align="center" class="heading">&nbsp;</h1>
</body>
</html>


<table align="center" cellpadding="0"  width="800" border="0">
  <tr>
    <td><br/><br/><h1 align="center" class="heading">"Welcome to Admin Panel"</h1>
      <p align="center">&nbsp;</p>
	<?php 
	 $id=$_REQUEST['id']; 
	 
	 $link=mysql_connect("localhost","root","") or die("Cannot Connect to the database!");
	
	 mysql_select_db("RMCET",$link) or die ("Cannot select the database!");
	 $query="SELECT * FROM student WHERE id='".$id."'";
		
		 $resource=mysql_query($query,$link) or die ("An unexpected error occured while <b>deleting</b> the record, Please try again!");
		  $result=mysql_fetch_array($resource);
		  
	 ?>
     <form id="form1" name="form1" method="get" action="modify3.php">
        <table align="center" width="291" border="0">
          
		  <tr>
            <td width="129"><strong>First Name:</strong></td>
            <td width="152"><input type="hidden" name="id" value="<?php echo $result[0] ?>"  />
            <label>
              <input name="name" type="text" id="textfield" value="<?php echo $result[1] ?>" />
            </label></td>
          </tr>

          <tr>
            <td><strong>middle Name:</strong></td>
            <td><input name="rollno" type="text" id="textfield2" value="<?php echo $result[2] ?>" /></td>
          </tr>
          <tr>
            <td><strong>Last Name:</strong></td>
            <td><input type="text" name="reg" id="textfield3" value="<?php echo $result[3] ?>" /></td>
          </tr>

          <tr>
            <td><strong>Username</strong></td>
            <td><input type="text" name="dept" id="textfield4" value="<?php echo $result[4] ?>" /></td>
          </tr>
		            <tr>
            <td><strong>Password:</strong>:</td>
            <td><input type="text" name="dept" id="textfield4" value="<?php echo $result[5] ?>" /></td>
          </tr>

          <tr>
            <td><strong>Email ID:</strong>:</td>
            <td><input type="text" name="dept" id="textfield4" value="<?php echo $result[6] ?>" /></td>
          </tr>

          <tr>
            <td><strong>Address</strong>:</td>
            <td><input type="text" name="dept" id="textfield4" value="<?php echo $result[7] ?>" /></td>
          </tr>

          <tr>
            <td><strong>Birthdate</strong>:</td>
            <td><input type="text" name="dept" id="textfield4" value="<?php echo $result[8] ?>" /></td>
          </tr>


          <tr>
            <td><strong>Mobile no:</strong>:</td>
            <td><input type="text" name="dept" id="textfield4" value="<?php echo $result[9] ?>" /></td>
          </tr>
		  
          <tr>
            <td><strong>Year</strong>:</td>
            <td><input type="text" name="dept" id="textfield4" value="<?php echo $result[10] ?>" /></td>
          </tr>

            <tr>
            <td><strong>Department</strong>:</td>
            <td><input type="text" name="dept" id="textfield4" value="<?php echo $result[11] ?>" /></td>
          </tr>

        </table>
        <p align="center">
          <label>
            <input type="submit" name="button" id="button" value="Modify" />
          </label>
        </p>
        <p align="center"><img onClick="javascript: history.go(-1)" border="0" src="images/cooltext457951462.png" alt="Go Back" onmouseover="this.src='images/cooltext457951462MouseOver.png';" onmouseout="this.src='images/cooltext457951462.png';" /></p>
      </form>

      </p>
      <p align="center"><a href="delete.php"><a href="../"></a></p>
      <p align="left">&nbsp;</p>
    <p align="left">&nbsp;</p></td>
  </tr>
</table>
<h1 align="center" class="heading">&nbsp;</h1>
</body>
</html>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Control Panel :: Student Information Panel:: Institute of Information Technology, BZU</title>
</head>

<body>

<br />
<br />
<br />
<table align="center" cellpadding="0" bgcolor="#FFFFFF" width="800" border="0">
  <tr>
    <td><h1 align="center" class="heading"><img src="images/cooltext457948700.png" width="747" height="58" alt="Welcome to Admin Panel" /></h1>
  <p align="center">
    <?php 

$id=$_REQUEST['id'];
$firstName=$_REQUEST['Fname'];
$middleName=$_REQUEST['Mname'];
$lastName=$_REQUEST['Lname'];
$username=$_REQUEST['username'];
$password=$_REQUEST['password'];
$emailId=$_REQUEST['email'];
$Address=$_REQUEST['Address'];
$Birthdate=$_REQUEST['Birthdate'];
$mobileNo=$_REQUEST['Mnumber'];
$Year=$_REQUEST['Year'];
$Department=$_REQUEST['Department'];

	 $link=mysql_connect("localhost","root","") or die("Cannot Connect to the database!");
	
	 mysql_select_db("RMCET",$link) or die ("Cannot select the database!");
	 $query="UPDATE student SET firstName='".$firstName."', middleName='".$middleName."',lastName='".$lastName."', username='".$username."', password='".$password."', emailId='".$emailId."', Address='".$Address."', Birthdate='".$Birthdate."', Mnumber='".$mobileNo."', Year='".$Year."',Department='".$Department."' WHERE id='".$id."'";
		
		  if(!mysql_query($query,$link))
		  {die ("An unexpected error occured while saving the record, Please try again!");}
		  else
		 {
		  echo "Record updated successfully!";}
	 ?>

      </p>
      <p align="center"><a href="./"><img border="0" src="images/cooltext457951462.png" onmouseover="this.src='images/cooltext457951462MouseOver.png';" onmouseout="this.src='images/cooltext457951462.png';" /></a><a href="../"><img border="0" src="images/cooltext457951615.png" onmouseover="this.src='images/cooltext457951615MouseOver.png';" onmouseout="this.src='images/cooltext457951615.png';" /></a></p>
      <p align="left">&nbsp;</p>
    <p align="left">&nbsp;</p></td>
  </tr>
</table>
<h1 align="center" class="heading">&nbsp;</h1>
</body>
</html>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Untitled Document</title>
</head>

<body>
<?php
 
	$f=$_POST['Fname'];
	$m=$_POST['Mname'];
	$l=$_POST['Lname'];
	$username=$_POST['Stusername'];
	$password=$_POST['Stpassword'];
    $E=$_POST['Year'];
	$Y=$_POST['Branch'];
	
	// Establish Connection with MYSQL
	$con = mysql_connect ("localhost","Staff","9821150615");
	// Select Database
	mysql_select_db("RMCET", $con);
	// Specify the query to Insert Record
	$sql = "insert into staff(firstName,middleName,lastName,username,password,Year,Department) values('".$f."','".$m."','".$l."','".$username."','".$password."','".$E."','".$Y."')";
	// execute query
	mysql_query ($sql,$con);
	// Close The Connection
	mysql_close ($con);
	
	echo '<script type="text/javascript">alert("Registration Completed Succesfully");window.location=\'insert.php\';</script>';

?>
</body>
</html>


<div id="container">
<div id='cssmenu'>
<ul>
         <li><a href='../index.php'><span>Home</span></a></li>

   <li class='active has-sub'><a href='#'><span>Photo Gallary</span></a>
                 <ul>
                     <li class='has-sub'><a href='#'><span>Event Photos</span></a>   </li>
                     <li class='has-sub'><a href='#'><span>Festival Photos</span></a>   </li>
                 </ul>
   </li>
               <li><a href='#'><span>Workshops</span></a></li>
			   <li><a href='#'><span>Attendence</span></a></li>
               <li class='active has-sub'><a href='#'><span>Important Notes</span></a>
			     <ul>
                     <li class='has-sub'><a href='#'><span>S.E</span></a>   </li>
                     <li class='has-sub'><a href='#'><span>T.E</span></a>   </li>
					 <li class='has-sub'><a href='#'><span>B.E</span></a>   </li>
                 </ul>
			   </li>
			   			   <li><a href='logout.php' align="right"><span align="right">Logout</span></a></li>
</ul> 

</div>
</html>
