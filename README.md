<html lang="es" xml:lang="es"dir="LTR" >
<head>
<META http-equiv="Content-Type" content="text/html; charset=utf-8"/>
<meta http-equiv="Content-Language" content="es" />
<link href="css/master.css" rel="stylesheet" type="text/css"/>
</head>
<body>

<style type="text/css">

</style>

<script>

var changes = false;

function setChange(){
     changes = true;
     var obj=document.getElementById('OKBtn');
     var obj1=document.getElementById('ApplyBtn');
     var body=document.getElementById('OKBtn_body');
     var body1=document.getElementById('ApplyBtn_body');
}

var global_value;

function checkChange(val) {
     if (global_value.length!=val.length) {
       setChange();
       return;
     }
     for(i=0;i< global_value.length;i++) {
       if(global_value.charAt(i) != val.charAt(i)) {
         setChange();
       }
     }
}

function ValidateFrm(){
if (document.frm.email.value.replace(/^\s*/, "").replace(/\s*$/, "").length==0) {
  alert("Introduzca su dirección de correo electrónico.");
  document.frm.email.focus();
  return false;
}
if (document.frm.problem_type.value==="none") {
  alert("Seleccione una categoría");
  document.frm.problem_type.focus();
  return false;
}
if (document.frm.subcategory.value==="none") {
  alert("Seleccione una subcategoría");
  document.frm.subcategory.focus();
  return false;
}
if (document.frm.title.value.replace(/^\s*/, "").replace(/\s*$/, "").length==0) {
  alert("Introduzca un título.");
  document.frm.title.focus();
  return false;
}
if (document.frm.desc.value.replace(/^\s*/, "").replace(/\s*$/, "").length==0) {
  alert("Introduzca una descripción.");
  document.frm.desc.focus();
  return false;
}
     return true;
}

function ExecuteOK(){
    if (! ValidateFrm())
      return;
    document.frm.OK.value = "OK";
    document.frm.submit();
}

function gotoPage(pageID) {
}
</script>
<table>

<form action="https://stratech.sysaidit.com:443/webformsubmit?pageEncoding=utf-8" method="post" name="frm">
<input type="hidden" name="X_TOKEN_stratech"  id="X_TOKEN_stratech"   value="69487162-e8e9-449a-adc8-d064ca1ed969"><input type="hidden" name="accountID" value="stratech" />
<input type="hidden" name="formID" value="64a1d9ed:1990633a44d:-33fe" />
<input type="hidden" name="reRoute" value="0"> <input type="hidden" name="parentPageName" value="WebFormHTML.jsp?idx=0" >
<input type="hidden" name="paneMessage" value="">
<input type="hidden" name="paneType" value="">
<input type="hidden" name="paneBtnArrayButtons" value="">
<input type="hidden" name="panePreSubmitFunc" value="">
<input type="hidden" name="paneTextRow" value=""><input type="hidden" name="centerPopup" value=""/><script src="https://stratech.sysaidit.com:443/calendar3.js" type="text/javascript" language="javascript"></script>
<script type="text/javascript" language="javascript" src="https://stratech.sysaidit.com:443/webformsubmit?getJS=YES&accountID=stratech&formID=64a1d9ed:1990633a44d:-33fe" >
</script>
  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Correo electrónico</td><td>&nbsp;&nbsp;<input name="email" type="text" onFocus="global_value=this.value" onChange="setChange();" onKeyUp="checkChange(this.value)" value="" size="50" maxlength="64"></td>
  </tr>  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Nombre</td><td>&nbsp;&nbsp;<input name="firstName" type="text" onFocus="global_value=this.value" onChange="setChange();" onKeyUp="checkChange(this.value)" value="" size="40" maxlength="40"></td>
  </tr>  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Apellidos</td><td>&nbsp;&nbsp;<input name="lastName" type="text" onFocus="global_value=this.value" onChange="setChange();" onKeyUp="checkChange(this.value)" value="" size="50" maxlength="50"></td>
  </tr>  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Categoría</td><td class="Form_Ctrl_Label">&nbsp;&nbsp;<select  name="problem_type"  onChange="setChange();updateSubCategory();">  <option value="none">Seleccione una categoría</option><option value="ATV MOSTRADOR" >ATV MOSTRADOR</option><option value="ATV SOM" >ATV SOM</option><option value="BANNER" >BANNER</option><option value="BANNER FDA" >BANNER FDA</option><option value="CLINIQUE" >CLINIQUE</option><option value="EN ESPERA" >EN ESPERA</option><option value="FS - PANTALLAS" >FS - PANTALLAS</option><option value="GONDOLA BEBES" >GONDOLA BEBES</option><option value="GONDOLA EMOTIVA" >GONDOLA EMOTIVA</option><option value="GONDOLA PREVENTIVA" >GONDOLA PREVENTIVA</option><option value="IOT - TELCEL" >IOT - TELCEL</option><option value="MARQUESINAS" >MARQUESINAS</option><option value="MEGA PANTALLAS" >MEGA PANTALLAS</option><option value="MONEX - BOTONERA" >MONEX - BOTONERA</option><option value="MONEX - CLICK SHARE" >MONEX - CLICK SHARE</option><option value="MONEX - LIENZO" >MONEX - LIENZO</option><option value="MONEX - PANTALLA DE TV" >MONEX - PANTALLA DE TV</option><option value="MONEX - PLAYERS COMUNICACIÓN INTERNA" >MONEX - PLAYERS COMUNICACIÓN INTERNA</option><option value="MONEX - PROYECTOR" >MONEX - PROYECTOR</option><option value="MONEX - SKY" >MONEX - SKY</option><option value="MONEX - TOTAL PLAY" >MONEX - TOTAL PLAY</option><option value="MONEX - VIDEOCONFERENCIAS" >MONEX - VIDEOCONFERENCIAS</option><option value="MONITOR" >MONITOR</option><option value="NUC" >NUC</option><option value="OPPO - TELCEL" >OPPO - TELCEL</option><option value="PANTALLA" >PANTALLA</option><option value="PLAYER  X10" >PLAYER  X10</option><option value="PLAYER BPX0" >PLAYER BPX0</option><option value="PLAYER DN" >PLAYER DN</option><option value="PLAYER DS" >PLAYER DS</option><option value="PLAYER SP0" >PLAYER SP0</option><option value="PLAYER ST" >PLAYER ST</option><option value="PLAYER SX" >PLAYER SX</option><option value="PLAYER X9" >PLAYER X9</option><option value="PLAYER X9W" >PLAYER X9W</option><option value="SBB" >SBB</option><option value="SERVICIOS DE TI (OFICINAS CORPORATIVAS)" >SERVICIOS DE TI (OFICINAS CORPORATIVAS)</option><option value="SERVICIOS DE TI PARA PUNTOS DE VENTA (POS)" >SERVICIOS DE TI PARA PUNTOS DE VENTA (POS)</option><option value="SMART BOX" >SMART BOX</option><option value="TURNOS - TELCEL" >TURNOS - TELCEL</option><option value="VIDEOWALL" >VIDEOWALL</option><option value="VIDEOWALL - TELCEL" >VIDEOWALL - TELCEL</option><option value="WALL BEBES" >WALL BEBES</option><option value="WALL EMOTIVO" >WALL EMOTIVO</option></select>&nbsp;<select name="subcategory" onChange="setChange();updateThirdLevelCategory();">  <option value="none">Seleccione una subcategoría</option><option value=" " > </option></select>&nbsp;<select name="thirdLevelCategory" onChange="setChange();thirdLevelChage();">  <option value="none">Seleccionar categoría de tercer nivel</option></select>
<input type="hidden" name="autoDescriptionTemplate" value="N">
</td>  </tr>  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Título</td><td>&nbsp;&nbsp;<input name="title" type="text" onFocus="global_value=this.value" onChange="setChange();" onKeyUp="checkChange(this.value)" value="" size="50" maxlength="100">
</td>  </tr>  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Descripción</td><td class="Form_Ctrl_Fields FieldBox">&nbsp;&nbsp;<textarea name="desc" cols="120" rows="5" id="desc" onchange="setChangeDesc(this);setChange(this);" onKeyUp="checkChangeDesc(this.value,this);checkChange(this.value,this);" onFocus="global_value=this.value" ></textarea>
</td>  </tr>  <tr>    <td colspan="2">&nbsp;</td>  </tr>  <tr >    <td colspan="1">&nbsp;      <table  class="Button3Parts" tabIndex="0" onclick="ExecuteOK();"><tbody class="Purple"><tr class=" - state - "><td class="ButtonFirst">&nbsp;</td><td class="ButtonLabel"><span>Enviar</span></td><td class="ButtonLast">&nbsp;</td></tr></tbody></table>           <input name="OK" type="hidden" value =""></td>  </tr>  <tr>    <td colspan="2">&nbsp;<br><p>&nbsp;&nbsp;&nbsp;&nbsp;Powered by SysAid <a href="http://www.ilient.com">Help Desk Software</a>.</p>  </td></tr>
</form>

</table>
</body>
</html>
