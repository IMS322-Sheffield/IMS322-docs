# Objects
We recently learned that [arrays](arrays.md) are useful for storing sequences of related data, such as GPS coordinates, enrollment figures, names of the months in a year, etc.

```js
let miamiGPS = [39.508930578260085, -84.73448077561027];

// Miami University undergraduate enrollment, 2018-2022 
let miamiEnrollment = [17327, 17246, 16522, 17003, 16864];

let months = ["January", "February", "March", "April", "May"]; // etc
```

The type of data and the relationship that those items have to each other suggest that an array is a suitable way to organize and store those items. They fit into a neat series and can be easily referenced using only the index (e.g. `months[0]` for the first month of the year, `months[1]` for the second month of the year, etc).

You may often want to store multiple pieces of information about a specific item that don't necessarily fall into a neat sequence. For example, if I were to try and save statistics about Miami University in an array, it would look kind of strange.

```js
let miamiOh = ["Public", 1809, "Oxford, OH", "Division I"];
```

You can likely guess what each item in that array means, but it would not necessarily be clear to someone who is not a student at Miami or doesn't know that the array contains data about a university. Also, it can become confusing to refer to non-sequential data by index number.

For cases like this, the *object* data type is usually much fitting. An object stores data in *key/value* pairs.

```js
// format is key: value

let miamiOh = {
  type: "Public",
  established: 1809,
  location: "Oxford, OH",
  ncaa: "Division I"
}
```

The *key*, which can be any string, is then used to reference the individual values using *dot notation*. This can provide much more clarity and helpful context than the generic index numbers used in an array.

```js
miamiOh.type;
// returns "Public"

miamiOh.established;
// returns 1809
```

You have already been using objects in much of the JavaScript code that you've previously written. Essentially, any time you have written something using *dot notation*, that is referencing the property (characteristic) of method (action it can perform) of an object.

```js
// the getElementById method of the document object
document.getElementById("text-input");

// the innerText property of the textInput object
textInput.innerText;
```

Try forking the embedded example below and changing the values within the object in the `script.js` file. Observe the changes in the console.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="vYPByeL" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYPByeL">
  Objects (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>