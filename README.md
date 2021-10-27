

window.onload = function(){

 empty_spots = document.querySelectorAll(".is-empty > .garage-vehicle > .garage-vehichleImage");


var names = [	"Travis’ Big Truck",
				"X1 Eclipse",
				"Hotdog Mobile",
			  "Vapor",
			  "8 Bit Racer",
			 //"The Gotham", 
             "The Pirc", 		 
             "Hang Eleven",	
             "‘31 Woodie Deluxx",  
             "Hange Fifteen",		
             "Wach 6", 		 
             "MSG 01",			 
             "Pumpkin Hauler", 	
             //"Corndog’s Car", 	
             "‘14 Mantaray", 		
             //"Ferreti Samsher 458",
             "Lacan Hypersport",
             "Hammer Wheels",
             "Mercedex McLaro SLR", 
             "I’m Spicy!", 	
             "Mercedex McLaro SLR 12.5", 
             "Nitr-o’-Lantern",	
             "Mercedex McLaro SHS 15.0",
             "Track-o’-Lantern",		
             "NitroPAC", 		
             "AU-79",			
            // "Lamborgotti Tiesto" ,
             "Wampus", 
             "Portch Cobalt",	
             "Alpha Romero 123Ω",	
             "Bright Idea",	
             "Gold Standard",		
             "Something Wicked",
             "The Danger"
        ]
        

var images = [/* 0 */ "https://www.nitrotype.com/cars/179_large_1.png",
					"https://www.nitrotype.com/cars/206_large_1.png",
					"https://www.nitrotype.com/cars/57_large_1.png",
					"https://www.nitrotype.com/cars/208_large_1.png",
			  /* 35 */"https://www.nitrotype.com/cars/50_large_1.png",
              /* 2 *///"https://www.nitrotype.com/cars/76_large_1.png",
              /* 3 */"https://www.nitrotype.com/cars/77_large_1.png",
              /* 4 */"https://www.nitrotype.com/cars/84_large_1.png",
              /* 5 */"https://www.nitrotype.com/cars/85_large_1.png",
              /* 6 */"https://www.nitrotype.com/cars/88_large_1.png",
              /* 7 */"https://www.nitrotype.com/cars/89_large_1.png",
              /* 8 */"https://www.nitrotype.com/cars/93_large_1.png",
              /* 10 */"https://www.nitrotype.com/cars/98_large_1.png",
              /* 11 *///"https://www.nitrotype.com/cars/104_large_1.png
              /* 12 */"https://www.nitrotype.com/cars/105_large_1.png",
              /* 13 *///"https://www.nitrotype.com/cars/106_large_1.png"
              /* 14 */"https://www.nitrotype.com/cars/107_large_1.png",
              /* 16 */"https://www.nitrotype.com/cars/110_large_1.png",
              /* 17 */"https://www.nitrotype.com/cars/124_large_1.png",
              /* 18 */"https://www.nitrotype.com/cars/127_large_1.png",
              /* 19 */"https://www.nitrotype.com/cars/129_large_1.png",
              /* 20 */"https://www.nitrotype.com/cars/130_large_1.png",
              /* 21 */"https://www.nitrotype.com/cars/137_large_1.png",
              /* 22 */"https://www.nitrotype.com/cars/141_large_1.png",
              /* 23 */"https://www.nitrotype.com/cars/155_large_1.png",
              /* 24 */"https://www.nitrotype.com/cars/163_large_1.png",
            		 "https://www.nitrotype.com/cars/97_large_1.png",
              /* 26 */"https://www.nitrotype.com/cars/177_large_1.png",
              /* 27 */"https://www.nitrotype.com/cars/178_large_1.png",
              /* 29 */"https://www.nitrotype.com/cars/180_large_1.png",
              /* 31 */"https://www.nitrotype.com/cars/185_large_1.png",
              /* 33 */"https://www.nitrotype.com/cars/191_large_1.png",
              /* 34 */"https://www.nitrotype.com/cars/203_large_1.png"
              ];
              
                  
    mkAct = document.querySelectorAll(".is-empty");
    
/*      var letsStart = setTimeout(function(){
for (let dt = 0; dt < names.length; dt++){
empty_spots[dt].setAttribute('data-tip', names[dt]);
}}, 10)
*/
 current_image = document.querySelector('.profile-car');

        //hover over car to see name of car
 /* for (var y = 0; y < mkAct; y++){
  document.querySelectorAll(".garage-vehichleImage")[y].setAttribute('data-tip', names[y]);
 }
 */
 
 var audio = new Audio('https://www.nitrotype.com/dist/site/misc/sounds/global/ogg/swoosh.ogg');
	 audio.volume = 0.5;
 var start = setTimeout(delay, 100)
 function delay(){
for(let r =0;r<images.length;r++){
	empty_spots[r].setAttribute('data-tip', names[r]);
	mkAct[r].addEventListener('click', function(){
			audio.play();
		setTimeout(function(){
	current_image.src = images[r];
	document.querySelector(".profile-carInterior > .mtm").innerHTML = names[r]; 
		}, 500);

	setTimeout(function(){
		current_image.classList.add("is-exiting");
		current_image.classList.remove("is-entering");
	}, 200)
setTimeout(function(){
		current_image.classList.add("is-entering");
		current_image.classList.remove("is-exiting");
}, 500) 

})
} 
}


//start

// stop

//...
/*
current_image = document.querySelector(".profile-car");
car = document.querySelectorAll(".garage-spot")
for (let crs = 0; crs < car.length; crs++){
car[crs].addEventListener("click", function(){
		current_image.classList.add("is-exiting");
setTimeout(function(){
		current_image.classList.remove("is-exiting");
		current_image.classList.add("is-intering");
},200) }
	)  
}
*/	
	
 // animate
 /*car = document.querySelector(".profile-car");
document.querySelectorAll(".garage-spot")[5].onclick = function(){
		car.classList.add("is-exiting");
setTimeout(function(){
		car.classList.remove("is-exiting");
		car.classList.add("is-intering");
},300)
}
*/
 // Fill the empty spots/
 
smallImage = images.map( a => a.replace("large","small") );
for (let i = 0; i < images.length; i++){
	empty_spots[i].style.backgroundImage = "url(" + smallImage[i] + ")";
	
	setTimeout(function(){
		
		mkAct[i].classList.remove("is-empty");
		var garage = document.querySelector(".garage");
var btns = garage.getElementsByClassName("garage-spot");
for (let i = 0; i < btns.length; i++) {
  btns[i].addEventListener("click", function() {
  var current = document.getElementsByClassName("is-active");
  if (current.length > 0) { 
    current[0].className = current[0].className.replace(" is-active", "");
  }
  this.className += " is-active";
  });
}
	}, 1000)
	
	//mkAct[i].className = "garage-spot";	
}
// setTimeout


// window end.. /
//};


//

// window end.. /
//};

// when you hover over the element
}

   // give names...

//test



      


      
