# Jquery

- Feather Lite

  - It reduces the complexcity of writing the code.
  - Example:

  ```js
  // Creating a element in JS
  window.addEventListner('DomContentLoaded', function () {
    let para = document.createElement('p');
    let text = document.createTextNode('This is a paragraph text');
    let ele = document.getElementById('target');
    para.appendChild(text);
    target.appendChild(para);
  });
  ```

  ```js
  // Creating an element in Jquery

  $('document').ready(function () {
    $('#target').append('<p>This is a paragraph text</p>');
  });
  ```

  This pretty sums up how lite the jquery is.

- Selectors and Filters

  - `selectors` select the part of the webpage.
  - `filters` refine the selected and targets the desired elements from the selected.

  ```js
  $('document').ready(function () {
    //Selectors
    $('p').css('border', '3px solid green');
    $('.heading').css('color', 'blue');
    //Filters
    $('p:first').css('border', '5px solid red');
    $('h3:not(#selectors)').css('color', 'violet');
  });
  ```

  - Basic selectors 

    ```js
    $('tagName'); //selects all the elements with that tag name.

    $('.className'); //selects all the elements with that class.

    $('#identifier'); //selects the elements with that id.

    $('tagName.className'); //selects all the elements with that tagname having matching class.

    $('tagName#id.className'); //selects all the elements of a tag having both matching id and class.

    $('*'); //selects all the elements in the page
    ```
      Examples : [Basic Selector Implementation](https://github.com/vvvk-gh/jquery/blob/master/BasicSelectors_finished.htm)

  - Basic Fiilters

    ```js
    :first, :last  // First and last of the given selector.

    :even, :odd //Only even or odd items in the matched set.

    :gt(), :lt(), :eq() //Items greter than, less than, or equal to an index.

    :animated  //Items that are in process of being animated.

    :focus //The element that currently has the focus.

    :not(expr) //Elements that dont match the given expression.
    ```
      Example : [Basic Filters Implementation](https://github.com/vvvk-gh/jquery/blob/master/BasicFilters_finished.html)

  - Hirarchy Selectors : Selects the element based on their position in DOM tree.

    They work by examining the position of target elements relative to the other elements.

    ```js
    $('parent > child'); //selects the direct child of the parent

    $('ancestor desendant'); //selects all the desendants down the line.

    $('prev + next'); //selects all the siblings and all sibilings down the line.

    $('prev ~ next'); //selects the adjcent sibiling to its previous.
    
    ```
    [Examples](https://github.com/vvvk-gh/jquery/blob/master/HierCombo_finished.html)

  - Attribute Selectors : Selects the elements in the webpage that have attribute values matching the criteria.

    ```JS
    $('ele[attr]');         //ele macthing attr (class, id )

    $('ele[(attr = val)]');  //ele has attr who value is val.

    $('ele[(attr ^= val)]'); //ele attr value starts with the val.

    $('ele[(attr *= val)]'); //ele attr value has any substring of val
    ```
    [Examples](https://github.com/vvvk-gh/jquery/blob/master/AttrFilters_finished.html)

  - Advanced Filters

    ```js
    :contains('text') //selects the ele the has the matching text.

    :has(selector) //selects atleast one ele that macthes the selector.

    :parent //selects ele that have atleast one child node (ele or text).

    :first-child, last-of-type //selects the ele based on the relations (fisrt child , last child of a parent ele)

    :nth-child(2) , nth-child(2n) //selects the child matching the mentioned index.
    ```
    [Examples](https://github.com/vvvk-gh/jquery/blob/master/ChildVisCont_finished.html)

- Traversing the documents with Jquery.

  ```js
  children(); // Retrives all the child ele's of the matched elements, expect text nodes.

  parents(), next(), prev(); //used to traverse the family relations of an element

  parentsUntil($('selector')); //get all the parent elements upto matched selector and the matched selector is not included.

  find('selector'); //searchs from the given ele to find the ele's that match the selector expression.

  each(callback); //loops over a set of matched ele's and calls the function for each one.
  ```
  [Example](https://github.com/vvvk-gh/jquery/blob/master/traversing_finished.html)

- Statement Chaining : call multiple functions on a single result set within the same line of code.
  ```js
  $('selector').fn1().fn2().fn3();
  ```
- Creating content :

  ```js
  html(str) or html(); //to set or retrive the html content on the page.
  //replaces the whole content with the given html string.

  text(str) or text(); //to set or retrive the text content of an ele
  ```
  [Examples](https://github.com/vvvk-gh/jquery/blob/master/creating_finished.htm)
  
  - Altering Document Content
  
  ```js
  
      wrap()            wrap the matched elements with the specified content
      
      wrapAll()         wrap content around the matched elements as a group
      
      unWrap()          remove the parents from the matched elements
      
      empty()           remove all the child elements from the matched elements
      
      remove()          removes elements from the page, including any embedded data and event handlers
      
      detach()          removes elements from the page, but maintains embedded data and event handlers
      
      replaceAll()      replaces the matched elements with the specified content
      
      replaceWith()     replaces matched elements with content or the results of a callback function
      
  ```
  [Examples](https://github.com/vvvk-gh/jquery/blob/master/altering_finished.htm)
  
    - Manipulating Document
    
    ```js
            
            attr(): get the value of an attribute

            attr(name,val) set the  name attribute to val

            attr({ name: val ... }) set multiple attributes in one call
              
            removeAttr(<i>name</i>)</code>: remove the attribute from the element
    ```
    [Examples](https://github.com/vvvk-gh/jquery/blob/master/attributes_finished.htm)
    
    - CSS functions
      
      ```js
        width() and height(): get or set the width/height of an element
        
        innerWidth() and innerHeight(): get or set the inner width/height of an element
        
        outerWidth() and outerHeight(): get the outer width/height of an element
        
        offset(): get coordinates of element relative to the document
        
        position(): get coordinates of element relative to the offset parent
        
      ```
      [Examples](https://github.com/vvvk-gh/jquery/blob/master/css_finished.htm)
      
     - Using the Data Methods
     
     ```js
      data() : To get all the data attributes on that selector
      
      data(key, value) : to get matching elements containg matching attribute value 
      
      removeData(key) : to remove the data attr from the elem.
     ```
    [Examples](https://github.com/vvvk-gh/jquery/blob/master/data_finished.html)
      
