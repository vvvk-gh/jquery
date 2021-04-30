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

    $('tagName.className'); //selects all the elements with that tagname having that class.

    $('tagName#id.className'); //selects all the elements of a tag having both id and class.
    ```
