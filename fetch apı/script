const url = 'https://script.google.com/macros/s/AKfycbyJzyd8cRNF5_Y34qLF7HzyWJg-BbszhEsd2DHdCMN_kFdGa6Z0/exec';
  
//google sheets urlden fetch ile json verileri çekme  
 async function getjss(){
      const response = await fetch(url);
      const data = await response.json();
     console.log(data);

      
//json verileri kullanılması
for (let index = 0; index < data.length; index++) {
let pcard = document.createElement("div");
pcard.classList.add("profile-card" , data[index].Mezuniyet_Yılı , data[index].Çalışıyor_musunuz , 
data[index].IsShow ,  "hidden" );
var pcont = $("<div/>").addClass("profile-content");

   //image div
   let pimg = document.createElement("div");
   pimg.classList.add("profile-image");
   //img tag
   let imgsrc = document.createElement("img");
   imgsrc.setAttribute("src", data[index].Profil_Fotoğrafı );
  
var desc1 = $("<h2/>").attr('id', 'isim').text(data[index].Ad_Soyad);
var tarih = $("<p/>").attr('id', 'tarih').text(data[index].Mezuniyet_Yılı);
var unvan = $("<p/>").attr('id', 'unvan').text(data[index].Pozisyon_Unvan);
var nçalış = $("<p/>").attr('id', 'nçalış').text(data[index].Çalıştığınız_Kurum);


//Çlışıyor-çalışmıyor
   var i = data[index].Çalışıyor_musunuz;
     if (i == "Çalışmıyor") {
      var çalışma = $("<p/>").attr('id', 'çalışma').text(data[index].Çalışıyor_musunuz);
     } else {
       çalışma = " ";
     }

var desc = $("<div/>").addClass("desc");
var btndiv = $("<div/>").addClass("btn-div");
var buton = $("<button/>").addClass("btn");

//sosyla medya var yok sorgu

  var i1 = data[index].Twitter_Hesabı;
    if (i1 == ""){
      var aTW = " ";
     } else {
       aTW = $("<a href = " + data[index].Twitter_Hesabı+ "/>");
     var tw = $("<i/>").attr('class', "fab fa-twitter");
    }


 var i2 = data[index].Facebook_Hesabı;
 if (i2 == ""){
  var aTW = " ";
} else {
 aFC = $("<a href = " + data[index].Facebook_Hesabı+ "/>");
 var fc = $("<i/>").attr('class', "fab fa-facebook");
}       

var i3 = data[index].Instagram_Hesabı;
if (i3 == ""){
 var aIG = " ";
} else {
aIG = $("<a href = " + data[index].Instagram_Hesabı+ "/>");
var ig = $("<i/>").attr('class', "fab fa-instagram");
}       

var i4 = data[index].Github_Hesabı;
if (i4 == ""){
 var aGH = " ";
} else {
aGH = $("<a href = " + data[index].Github_Hesabı+ "/>");
var gh = $("<i/>").attr('class', "fab fa-github");
}       

var i5 = data[index].Linkedin_Hesabı;
if (i5 == ""){
 var aLK = " ";
} else {
aLK = $("<a href = " + data[index].Linkedin_Hesabı+ "/>");
var lk = $("<i/>").attr('class', "fab fa-linkedin");
}       

var i6 = data[index].Özgeçmiş_Dosyası;
if (i6 == ""){
 var aFİLE = " ";
} else {
aFİLE = $("<a href = " + data[index].Özgeçmiş_Dosyası+ "/>");
var file = $("<i/>").attr('class', "fa-solid fa-file");
}       

var i7 = data[index].Web_Sayfası;
if (i7 == ""){
 var aWEB = " ";
} else {
aWEB = $("<a href = " + data[index].Web_Sayfası+ "/>");
var web = $("<i/>").attr('class', "fa-solid fa-earth-americas");
}  

var myFinalVar =

//alt divleri ana div e gönderme 
$(pcard).append(pcont);
$(pcont).append(pimg);
$(pimg).append(imgsrc);
$(pcont).append(desc);
$(pcont).append(btndiv);
$(desc).append(desc1);
$(desc).append(tarih);
$(desc).append(unvan);
$(desc).append(nçalış);
$(desc).append(çalışma);
//sosyla medya btn
$(btndiv).append(buton);
$(buton).append(aTW);
$(buton).append(aGH);
$(buton).append(aFC);
$(buton).append(aIG);
$(buton).append(aLK);
$(buton).append(aFİLE);
$(buton).append(aWEB);
$(aFC).append(fc);
$(aTW).append(tw);
$(aIG).append(ig);
$(aGH).append(gh);
$(aLK).append(lk);
$(aFİLE).append(file);
$(aWEB).append(web);

$(myFinalVar).appendTo(".users");

}
}
getjss()

//mezuniyet yılı filtreleeme
function filterProduct(value) {

  let buttons = document.querySelectorAll(".button-value");
  buttons.forEach((button) => {

    if (value.toUpperCase() == button.innerText.toUpperCase()) {
      button.classList.add("active");
    } else {
      button.classList.remove("active");
    }
  });

  let elements = document.querySelectorAll(".profile-card");

  elements.forEach((element) => {

    if (value == "all") {
       
      element.classList.remove("hide");
    } else {
      //Check if element contains category class
      if (element.classList.contains(value)) {
         
        //display element based on category
        element.classList.remove("hide");
      } else {
        //hide other elements
        element.classList.add("hide");
      }
    }
  });
}

window.onload = () => {
  filterProduct("all");
};


//çalışıyor çalışmıyor filtreleme
function filterProduct2(value) {

  let buttons2 = document.querySelectorAll(".button-value2");
  buttons2.forEach((button2) => {
   
    if (value.toUpperCase() == button2.innerText.toUpperCase()) {
      button2.classList.add("active");
    } else {
      button2.classList.remove("active");
    }
  });
 
  let elements = document.querySelectorAll(".profile-card");
 

  elements.forEach((element) => {

    if (value == "all") {
       
      element.classList.remove("hide");
    } else {
     
      if (element.classList.contains(value)) {
        
        
        element.classList.remove("hide");
      } else {
      
        element.classList.add("hide");
      }
    }
  }
  );
}

window.onload = () => {
  filterProduct2("all");
};



