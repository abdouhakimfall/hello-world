var n = parseInt(readline());
var inputs = readline().split(' ');
var val=Array(n);
for (var i = 0; i < n; i++) { //Récupération des valeurs en entrée
     val[i] = parseInt(inputs[i]);    
}

var min=val[1]-val[0]; //initialisation de la variable min
//On parcours toutes les valeurs pour calculer la perte maximale
for(var i=0;i<n-1;i++){
    for(var j=i+1;j<n;j++){
        if(val[j]-val[i]<min) min=val[j]-val[i];
    }
min=(min<0)*min; //Test logique s'il y a perte ou gain

print(min);
