# Bootstrap
Bootstrap is the most well known and most used CSS framework of all time (as of this current date). Its focus is on creating a toolkit of predefined classes and objects that
can essentially be copy-pasted from the docs and inserted directly into the programmer's code. This means that Bootstrap is, by design, a plug-and-play solution to building websites, one that is portable, widely used, and responsive while requiring minimal maintenance or programmer work. Additionally, Bootstraps documentation may be the most in depth of any CSS frameworks.

# Utility API
This [framework](https://getbootstrap.com/docs/5.0/utilities/api/) was developed for recent versions of Bootstrap, and seeks to bridge the gap between frameworks that obfuscate away much of the actual CSS (Bootstrap) and utility-first frameworks that require significant tinkering on the programmer's part (Tailwind). At its core, Bootstrap uses Sass to build and control its internal CSS frameworks. What the utility API does is allow the programmer greater access into the internal workings of Bootstrap and its Sass compilation. 

For example, in the following code, the utility API is used to change the `opacity` class prefix is changed to `o`

```
$utilities: (
  "opacity": (
    property: opacity,
    class: o,
    values: (
      0: 0,
      25: .25,
      50: .5,
      75: .75,
      100: 1,
    )
  )
);
```

And the result:
```
.o-0 { opacity: 0 !important; }
.o-25 { opacity: .25 !important; }
.o-50 { opacity: .5 !important; }
.o-75 { opacity: .75 !important; }
.o-100 { opacity: 1 !important; }
```

# Modular and Prebuilt Object Design
Bootstrap was created to be easy to get running, easy to maintain, and easy to theme. Given that all Bootstrap elements (such as buttons, dropdowns, and tables) are already pre-themed in the imported Bootstrap assets, a programmer doesn't have to spend time making sure each element of a website interacts correctly with and looks like the other parts. This approach has upsides and downsides, but for programmers seeking ease of maintenance and setup, Bootstrap is a solid choice.

There is also a focus on code modularity, as shown [here](https://getbootstrap.com/docs/5.2/components/carousel/#with-controls) and [here](https://getbootstrap.com/docs/5.2/components/carousel/#with-controls), adding in an carousel's indicator that shows which slide it's on is as easy as copy-pasting the following code into the main carousel container:

```
<div class="carousel-indicators">
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
</div>
```
The programmer doesn't have to modify the carousel elements, and can remove or include other Bootstrap CSS additions wherever they want. This modular design is echoed throughout Bootstrap's framework, regardless of the objects being worked with. This means that Bootstrap is probably the best choice for programmers who just want to set up a front end for a website, have it already pre-themed, and then make minor modifications to suit their needs.
