# Denjakaal88<br>
TETAPLAH BERNAPAS JANGAN LUPA BERNAPAS<br>
NIM : 1811500055<br>
NAMA : KUKUH KURNIAWAN<br>
KEL : TI6A<br>
<br>
PT 1<br>
NIM : 1811500055<br>
NAMA : KUKUH KURNIAWAN<br>
KEL : TI6A<br>
<br>
PT 2<br>
NIM : 1811500055<br>
NAMA : KUKUH KURNIAWAN<br>
KEL : TI6A<br>
<br>
PT 3<br>
NIM : 1811500055<br>
NAMA : KUKUH KURNIAWAN<br>
KEL : TI6A<br>
<br>
PT 4<br>
NIM : 1811500055<br>
NAMA : KUKUH KURNIAWAN<br>
KEL : TI6A<br>
<br>
PT 5<br>
NIM : 1811500055<br>
NAMA : KUKUH KURNIAWAN<br>
KEL : TI6A<br>
<br>
PT 6<br>
NIM : 1811500055<br>
NAMA : KUKUH KURNIAWAN<br>
KEL : TI6A<br>


function Simpan() {
  var Sheet = SpreadsheetApp.getActiveSpreadsheet();
  var shtinput = Sheet.getSheetByName('Input');
  var shtdb = Sheet.getSheetByName('Database');
  
  var id = shtinput.getRange('D3').getValue();
  var nama = shtinput.getRange('D5').getValue();
  var tgl = shtinput.getRange('D7').getValue();
  var alamat =  shtinput.getRange('D9').getValue();
  var sekolah = shtinput.getRange('D11').getValue();
  
  var baris = shtdb.getRange('F1').getValue();
  baris += 1;
  var rangeisi = shtdb.getRange('A' + baris + ':E'+ baris);
  rangeisi.setValues([[id,nama,tgl,alamat,sekolah]]);
  bersih();
}

function bersih() {
  var Sheet = SpreadsheetApp.getActiveSpreadsheet();
  var shtinput = Sheet.getSheetByName('Input');
  
  shtinput.getRange('D3').clearContent();
  shtinput.getRange('D5').clearContent();
  shtinput.getRange('D7').setValue('1/1/2000');
  shtinput.getRange('D9').clearContent();
  shtinput.getRange('D11').clearContent();
}
