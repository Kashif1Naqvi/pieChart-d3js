# pieChart-d3js
d3JS version=5
See the Demo =>  https://bl.ocks.org/Kashif1Naqvi/raw/318fe0b1c691c4c2d5e90c09646e58c7/328f9f706c21cd4fb07dcaa9b616abc87b2ba872/

chart is created hirarical form 

like this

d3.hirarchy("data that we target").sum("target the value of chart data " d => d.value)

use this in pure function

I'm using d3 version 5 when first time I try to access data in D3 then show me errors, so it's important to tell you how to fetch JSON in 
D3js version 5

d3.json("path of json file").then( // callBack function in which you access everyThing that you want from json file d=>{
  console.log(d)
// show all data in json file



})


some importats points 
If you try to understand the code, then understand easily 
divide code into small pieces firstly understand 
Svg how created
then understand how root variable created 
basically all data will be created  on the base of root variable 

root variable target the pure function name partition() in which we pass the data

function partition(d){
  let root = d3.hierarchy(d)
    .sum(d=>d.value)
    .sort((a,b)=>b.avalue - a.value)
  return d3.partition().size([2 * Math.PI , root.height + 1  ])(root)
    
}

like
const root = partition(d)
then access all hierarchy data :) 

console.log(root)
