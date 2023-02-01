# assignment2-ravuri
# Lakshmi Karthik Ravuri 
###### Volley ball INDIA

i like **volley ball** because i **can play** only that

---

### Sport Details
1. India men's national volleyball team
   1. Balwanth Singh
   2. Shyam Sunder Rao
   3. Jimmy George
* Spiking Sensations
* Bumpin' Bettas
* Diggin' Divas
* Setting Stars 

[Link to Aboutme File](https://github.com/ravuril/assignment2-ravuri/blob/main/AboutMe.md)

---

## Table Section countries to visit

Below are the some of the best countries to visit during your vaccation

| Country Name | Reason |  Days to Spend |
|--------------|--------|---------------:|
| Maldives | It has more than 1,000 islands, thatched-roof bungalows and a romantic atmosphere | 4 |
| Paris |  Travelers really fall in love with the city's quaint cafes, vibrant markets | 3 |
| Bora Bora | A small French Polynesian island may lack in size it makes up in sheer tropical beauty| 3 |
| London | The best time to travel to London is during the warmer months. | 4 |

---

##  Pithy Quotes section
>No man has a good enough memory to be a successful liar. *Abraham Lincoln*

>Age is something that doesn't matter unless you are a cheese. *Luis Bunuel*

---

## Code Fencing Section
 >Modify Canvas SVG Image with Javascript

 [Link to stackoverflow article](https://stackoverflow.com/questions75274984modify-canvas-svg-image-with-javascript)

 ``` const canvas = document.getElementById('canvas');
 const ctx = canvas.getContext('2d');

 fetch('data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTAgMTAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CiAgPHBhdGggZD0iTSA1IDAgTCAwIDUgTCA1IDEwIEwgMTAgNSBaIiAvPgo8L3N2Zz4=')
  .then(response => response.text())
  .then(text => {
    let xmlDoc = new DOMParser().parseFromString(text,'text/xml');
    changeAttribute(xmlDoc, '//svg:path', {fill:'red'});
    changeAttribute(xmlDoc, '//svg:svg', {width:100, height:100});
    insertIntoCanvas(xmlDoc);
  });

 function insertIntoCanvas(xmlDoc){
  let file = new File([xmlDoc.rootElement.outerHTML], 'svg.svg', {
    type: "image/svg+xml"
  });
  // and a reader
  let reader = new FileReader();
  
  reader.addEventListener('load', e => {
    /* create a new image assign the result of the filereader
    to the image src */
    let img = new Image();
    // wait for it to got load
    img.addEventListener('load', e => {
      // update canvas with new image
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      ctx.drawImage(e.target, 0, 0);
    });
    img.src = e.target.result;
  });
  // read the file as a data URL
  reader.readAsDataURL(file);
 }

 function changeAttribute(doc, xpath, obj) {
  let r = doc.evaluate(xpath, doc, nsResolver, XPathResult.ANY_TYPE, null);

  let nodes = [];
  let next = r.iterateNext();
  while (next) {
    nodes.push(next);
    next = r.iterateNext();
  }

  nodes.forEach(node => {
    Object.keys(obj).forEach(key => {
      node.setAttribute(key, obj[key]);
    });
  });
 }

 function nsResolver(prefix) {
  const ns = {
    'xhtml': 'http://www.w3.org/1999/xhtml',
    'svg': 'http://www.w3.org/2000/svg'
  };
  return ns[prefix] || null;
 } 
 ```

[Link to code snippet](https://stackoverflow.com/questions75274984modify-canvas-svg-image-with-javascript)