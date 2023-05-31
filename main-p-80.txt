
names_of_people = [];
    
function Submit()
{
     
    var GuestName = document.getElementById("name1").value;
    console.log(GuestName);
    names_of_people.push(GuestName);
    
    console.log(names_of_people);
    document.getElementById("display_name").innerHTML = names_of_people;
    document.getElementById("name1").value=" ";
  
}

function show()
{
    var invitado_array = [];

    var longitud_names_of_people = names_of_people.length;
    console.log(longitud_names_of_people);

    for (var k = 0; k < longitud_names_of_people; k++)
    {
        var r= k + 1;
        invitado_array.push( r + ".-" + names_of_people[k]+ "<br>");
        console.log(invitado_array);
    }

    var remover_comas = invitado_array.join(" ");
    console.log(remover_comas);
    document.getElementById("p1").innerHTML = remover_comas;
}

function sorting()
{
    
    names_of_people.sort();
    console.log(names_of_people);
    
    var invitado_array_ordenar = [];

    var longitud_names_of_people = names_of_people.length;
    console.log(longitud_names_of_people);

    for (var k = 0; k < longitud_names_of_people; k++)
    {
        var r= k + 1;
        invitado_array_ordenar.push( r + ".-" + names_of_people[k]+ "<br>");
        console.log(invitado_array_ordenar);
    }

    var remover_comas = invitado_array_ordenar.join(" ");
    console.log(remover_comas);
    document.getElementById("sorted").innerHTML = remover_comas;
}



function searching()
{
    var s= document.getElementById("s1").value;
    var found = 0;
    var j;
    for(j = 0; j < names_of_people.lenght; j++)
    {
        if(s = names_of_people[j])
        {
            found = found + 1;
        }
         document.getElementById("p2").innerHTML="name found " + s +" time/s";
        console.log("found name " + found + " time/s");
        
    }
    
}