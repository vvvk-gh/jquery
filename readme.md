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

  - Basic Fiilters

    ```js
    :first, :last  // First and last of the given selector.

    :even, :odd //Only even or odd items in the matched set.

    :gt(), :lt(), :eq() //Items greter than, less than, or equal to an index.

    :animated  //Items that are in process of being animated.

    :focus //The element that currently has the focus.

    :not(expr) //Elements that dont match the given expression.
    ```

  - Hirarchy Selectors : Selects the element based on their position in DOM tree.

    They work by examining the position of target elements relative to the other elements.

    ```js
    $('parent > child'); //selects the direct child of the parent

    $('ancestor desendant'); //selects all the desendants down the line.

    $('prev + next'); //selects all the siblings and all sibilings down the line.

    $('prev ~ next'); //selects the adjcent sibiling to its previous.
    ```

  - Attribute Selectors : Selects the elements in the webpage that have attribute values matching the criteria.

    ```JS
    $('ele[attr]');         //ele macthing attr (class, id )

    $('ele[(attr = val)]');  //ele has attr who value is val.

    $('ele[(attr ^= val)]'); //ele attr value starts with the val.

    $('ele[(attr *= val)]'); //ele attr value has any substring of val
    ```

  - Advanced Filters

    ```js
    :contains('text') //selects the ele the has the matching text.

    :has(selector) //selects atleast one ele that macthes the selector.

    :parent //selects ele that have atleast one child node (ele or text).

    :first-child, last-of-type //selects the ele based on the relations (fisrt child , last child of a parent ele)

    :nth-child(2) , nth-child(2n) //selects the child matching the mentioned index.
    ```

- Traversing the documents with Jquery.

  ```js
  children(); // Retrives all the child ele's of the matched elements, expect text nodes.

  parents(), next(), prev(); //used to traverse the family relations of an element

  parentsUntil($('selector')); //get all the parent elements upto matched selector and the matched selector is not included.

  find('selector'); //searchs from the given ele to find the ele's that match the selector expression.

  each(callback); //loops over a set of matched ele's and calls the function for each one.
  ```
