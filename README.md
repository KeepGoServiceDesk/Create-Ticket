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
if (document.frm.firstName.value.replace(/^\s*/, "").replace(/\s*$/, "").length==0) {
  alert("Introduzca Nombre");
  document.frm.firstName.focus();
  return false;
}
if (document.frm.lastName.value.replace(/^\s*/, "").replace(/\s*$/, "").length==0) {
  alert("Introduzca Apellidos");
  document.frm.lastName.focus();
  return false;
}
if (document.frm.cellphone.value.replace(/^\s*/, "").replace(/\s*$/, "").length==0) {
  alert("Introduzca Teléfono móvil");
  document.frm.cellphone.focus();
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
<input type="hidden" name="formID" value="64a1d9ed:1990633a44d:-5d6c" />
<input type="hidden" name="reRoute" value="0"> <input type="hidden" name="parentPageName" value="WebFormHTML.jsp?idx=0" >
<input type="hidden" name="paneMessage" value="">
<input type="hidden" name="paneType" value="">
<input type="hidden" name="paneBtnArrayButtons" value="">
<input type="hidden" name="panePreSubmitFunc" value="">
<input type="hidden" name="paneTextRow" value=""><input type="hidden" name="centerPopup" value=""/><script src="https://stratech.sysaidit.com:443/calendar3.js" type="text/javascript" language="javascript"></script>
<script type="text/javascript" language="javascript" src="https://stratech.sysaidit.com:443/webformsubmit?getJS=YES&accountID=stratech&formID=64a1d9ed:1990633a44d:-5d6c" >
</script>
  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Nombre</td><td>&nbsp;&nbsp;<input name="firstName" type="text" onFocus="global_value=this.value" onChange="setChange();" onKeyUp="checkChange(this.value)" value="" size="40" maxlength="40"></td>
  </tr>  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Apellidos</td><td>&nbsp;&nbsp;<input name="lastName" type="text" onFocus="global_value=this.value" onChange="setChange();" onKeyUp="checkChange(this.value)" value="" size="50" maxlength="50"></td>
  </tr>  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Teléfono móvil</td><td>&nbsp;&nbsp;<input name="cellphone" type="text" onFocus="global_value=this.value" onChange="setChange();" onKeyUp="checkChange(this.value)" value="" size="32" maxlength="32"></td>
  </tr>  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Título</td><td>&nbsp;&nbsp;<input name="title" type="text" onFocus="global_value=this.value" onChange="setChange();" onKeyUp="checkChange(this.value)" value="" size="50" maxlength="100">
</td>  </tr>  <tr><td colspan="2">&nbsp;</td></tr>  <tr>    <td class="Form_Ctrl_Label" >&nbsp;&nbsp;&nbsp;&nbsp;Descripción</td><td class="Form_Ctrl_Fields FieldBox">&nbsp;&nbsp;<textarea name="desc" cols="120" rows="5" id="desc" onchange="setChangeDesc(this);setChange(this);" onKeyUp="checkChangeDesc(this.value,this);checkChange(this.value,this);" onFocus="global_value=this.value" ></textarea>
</td>  </tr>  <tr>    <td colspan="2">&nbsp;</td>  </tr>  <tr >    <td colspan="1">&nbsp;      <table  class="Button3Parts" tabIndex="0" onclick="ExecuteOK();"><tbody class="Purple"><tr class=" - state - "><td class="ButtonFirst">&nbsp;</td><td class="ButtonLabel"><span>Enviar</span></td><td class="ButtonLast">&nbsp;</td></tr></tbody></table>           <input name="OK" type="hidden" value =""></td>  </tr>  <tr>    <td colspan="2">&nbsp;<br><p>&nbsp;&nbsp;&nbsp;&nbsp;Powered by SysAid <a href="http://www.ilient.com">Help Desk Software</a>.</p>  </td></tr>
</form>

</table>
</body>
</html>
