# Dom Builder

Builds a DOM element with Javascript Code in simple way ten return DOM element .

These Library Main Uses These Helper : https://github.com/abdullahalnahhal/PHPHelper.js


    var  element = new DomBuilder('form', {
        "method" : "post",
        "action" : "https://github.com/abdullahalnahhal",
        "id" : "dom-builder-form"
    });

    element
    .child('textarea', {
        "name" : "thank-message",
        "class" : "pla pla",
    }, "thank you Abdullah")
    .child('br', {})
    .child('button', {
        "class" : "btn btn-success",
        "type" : "submit"
    }, "Submit ... !");

    console.log (element.draw());
    /* 
        <form method="post" action="https://github.com/abdullahalnahhal" id="dom-builder-form">
            <textarea name="thank-message" class="pla pla">thank you Abdullah</textarea>
            <br>
            <button class="btn btn-success" type="submit">Submit ... !</button>
        </form>
    */
    document.querySelector('body').appendChild(element.draw());


<form method="post" action="https://github.com/abdullahalnahhal" id="dom-builder-form">
    <textarea name="thank-message" class="pla pla">thank you Abdullah</textarea>
    <br>
    <button class="btn btn-success" type="submit">Submit ... !</button>
</form>

---

**Method : child**

adds child to the element

    DomBuilder child(element, attributes, text = null)

**Parameters :**
    
- { string } element : element wanted to be created 
  - example : `'div' , 'table' , 'form', ... etc` .
- { Object } attributes : attributes object
  - example : `{"id" : "...","name" : "...",...}`
- {string} text : element text content
  - default : null
  - example : `"Hello World ... !"`.
  
**Return : DomBuilder** `the same object`

---

**Method : draw**

returns the DOM element

    DOMObject draw()

**Return : DOMObject** `the same object`

    Exmple : <button class="btn btn-success" type="submit">Submit ... !</button>

---

**Method : getChildren**

returns the child list

    DomBuilder[] getChildren()

**Return : DomBuilder [ ]** `array of DomBuilder Objects` 

---

**Method : getFirstChild**

returns the first child into element

    DomBuilder getFirstChild()

**Return : DomBuilder** `DomBuilder Objects` 

---

**Method : getLastChild**

returns the last child of the element

    DomBuilder getLastChild()

**Return : DomBuilder** `DomBuilder Objects` 
