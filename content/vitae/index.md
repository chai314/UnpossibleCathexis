---
title: "Résumé"
date: 2024-08-27
draft: false

showDate : false
showHeadingAnchors : false
showPagination : false
showReadingTime : false
showTableOfContents : true
showTaxonomies : false 
showWordCount : false
summary: "Curriculum vitae"
showViews: false
layoutBackgroundHeaderSpace: false
showAuthor: false

---


<style>
.square {
  width: 100px;
  height: 100px;
  object-fit: contain;
  background-color: white;
}
.square2 {
  width: 100px;
  height: 100px;
  object-fit: cover;
}
.table-container {
  display: table;
  width: 100%;
}
.table-row {
  display: table-row;
}
.table-cell {
  display: table-cell;
  vertical-align: middle;
  padding: 5px;
  text-align: center;
}
.new-icon {
  background-color: #007BFF;
  color: white;
  font-size: 0.8em;
  padding: 3px 6px;
  border-radius: 5px;
  margin-right: 8px;
}
</style>

## Experience

<div class="table-container">
    <div class="table-row">
    <div class="table-cell"><strong></strong></div>
    <div class="table-cell"><strong>Firm</strong></div>
    <div class="table-cell"><strong>Role</strong></div>
    <div class="table-cell"><strong>Year</strong></div>
    </div>

  <div class="table-row">
    <div class="table-cell"><img class="square" src="sfdc.png" /></div>
    <div class="table-cell">Salesforce Inc.</div>
    <div class="table-cell">Summer<br>Intern</div>
    <div class="table-cell">upcoming!</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img class="square" src="tifr.png" /></div>
    <div class="table-cell">Tata Institute of<br>Fundamental Research</div>
    <div class="table-cell">VSRP<br>Scholar</div>
    <div class="table-cell">2024</div>
  </div>
</div>

## Stuff

{{< timeline >}}

{{< timelineItem icon="github" header="GitHub" >}}
{{<github1 repo="chai314/UnpossibleCathexis">}}
{{< /timelineItem >}}

{{< timelineItem icon="code" header="Tech" >}}
{{< gallery >}}
  <img src="python.svg" class="grid-w20" />
  <img src="c.svg" class="grid-w20" />
  <img src="latex.png" class="grid-w33" />
  <img src="cpp.svg" class="grid-w20" />
  <img src="sage.png" class="grid-w20" />
  <img src="mysql.svg" class="grid-w20" />
  <img src="tensorflow.svg" class="grid-w20" />
  <img src="git.svg" class="grid-w20" />
  <img src="haskell.svg" class="grid-w20" />
{{< /gallery >}}
{{< /timelineItem >}}

{{< timelineItem header="I click colors in my free time">}}

<style>
    .row-container {
        display: flex;
        gap: 10px;
        margin: 20px;
        width: 100%;
        cursor: pointer; /* Indicate clickability */
    }

    .swatch {
        flex: 1;
        height: 50px;
        border-radius: 5px;
        position: relative;
        transition: background-color 0.5s ease, transform 0.2s ease;
        transform-origin: bottom center;
    }

    /* Jelly bounce animation */
    @keyframes jellyBounce {
        0% {
            transform: translateY(0) scale(1);
        }
        30% {
            transform: translateY(30px) scale(1.05, 0.95); /* Compress on downward motion */
        }
        50% {
            transform: translateY(0) scale(1); /* Return to normal */
        }
        70% {
            transform: translateY(15px) scale(0.95, 1.05); /* Slight overshoot */
        }
        100% {
            transform: translateY(0) scale(1); /* Back to rest */
        }
    }

    .wave-animation-1 {
        animation: jellyBounce 2s cubic-bezier(.5, .05, .1, .3) infinite;
    }

    .wave-animation-2 {
        animation: jellyBounce 2s cubic-bezier(.5, .05, .1, .3) infinite;
        animation-delay: 0.3s; /* Phase shift for second swatch */
    }

    .wave-animation-3 {
        animation: jellyBounce 2s cubic-bezier(.5, .05, .1, .3) infinite;
        animation-delay: 0.6s; /* Phase shift for third swatch */
    }
</style>

<div id="row1" class="row-container"></div>

<script>
    const row = document.getElementById('row1');
    let currentTheme = 0;

    // Base colors for the themes
    const baseColors = {
        blue: [200, 50, 60],  // Blue tone
        red: [0, 50, 70],     // Red tone
        amethyst: [270, 60, 70], // Purple/Amethyst tone
        bright: [50, 100, 70], // Bright yellows, oranges
        light: [150, 100, 70]   // Light and pastel-like
    };

    const themes = ['blue', 'red', 'amethyst', 'bright', 'light'];

    function getRandomColor(baseHue, baseSaturation, baseLightness) {
        const hue = baseHue + (Math.random() * 40 - 13); 
        const saturation = baseSaturation + (Math.random() * 25 - 12);        const lightness = baseLightness + (Math.random() * 45 - 22);

        return `hsl(${hue}, ${saturation}%, ${lightness}%)`;
    }

    // a random color based on current theme
    function generateSwatch(index) {
        const theme = themes[currentTheme];
        const [baseHue, baseSaturation, baseLightness] = baseColors[theme];
        const randomColor = getRandomColor(baseHue, baseSaturation, baseLightness);
        const swatch = document.createElement('div');
        swatch.className = 'swatch';
        swatch.style.backgroundColor = randomColor;
        swatch.classList.add(`wave-animation-${index + 1}`);
        return swatch;
    }

    //  randomize swatch colors
    function changeTheme() {
        currentTheme = (currentTheme + 1) % themes.length; // Cycle through themes
        const swatches = document.querySelectorAll('.swatch');
        swatches.forEach((swatch, index) => {
            const theme = themes[currentTheme];
            const [baseHue, baseSaturation, baseLightness] = baseColors[theme];
            swatch.style.backgroundColor = getRandomColor(baseHue, baseSaturation, baseLightness);
        });
    }

    row.addEventListener('click', changeTheme);
    for (let i = 0; i < 3; i++) {
        row.appendChild(generateSwatch(i));
    }
</script>



{{< /timelineItem >}}

{{< /timeline >}}


## Courses I Took
(read: survived)

<div class="table-container">
<div class="table-row">
  <div class="table-cell"><strong>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <!-- This is peak HTML. -->
  </strong></div>
  <div class="table-cell"><strong>Code</strong></div>
  <div class="table-cell"><strong>Name</strong></div>
  <div class="table-cell"><strong>Commentary</strong></div>
</div>

<div class="table-row">
  <div class="table-cell">
    <img class="square2" src="321.png" />
  </div>
  <div class="table-cell">
    <span class="new-icon">EW</span> MA321
  </div>
  <div class="table-cell">Optimization</div>
  <div class="table-cell">The worst.</div>
</div>

<div class="table-row">
  <div class="table-cell">
    <img class="square2" src="371.png" />
  </div>
  <div class="table-cell">
    <span class="new-icon">NEW</span> MA371
  </div>
  <div class="table-cell">Stochastic<br>Calculus</div>
  <div class="table-cell">First fun finance course.<br>Shreve's a hero</div>
</div>

<div class="table-row">
  <div class="table-cell">
    <img class="square2" src="323.png" />
  </div>
  <div class="table-cell">
    <span class="new-icon">NEW</span> MA323
  </div>
  <div class="table-cell"><a href="https://github.com/chai314/marco-polo">Monte Carlo</a></div>
  <div class="table-cell">Never forget we asked prof to download default libraries</div>
</div>

  <div class="table-row">
    <div class="table-cell"><img class="square2" src="411.png" /></div>
    <div class="table-cell">MA411</div>
    <div class="table-cell">Differential<br>Geometry</div>
    <div class="table-cell">So pissed at morning labs.</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img class="square2" src="anjankc.png" /></div>
    <div class="table-cell">MA641</div>
    <div class="table-cell">Operator Theory<br>on Hilbert Spaces</div>
    <div class="table-cell">He's actually the best.</div>
  </div>
  
  
  <div class="table-row">
    <div class="table-cell"><img class="square2" src="271.png" /></div>
    <div class="table-cell">MA271</div>
    <div class="table-cell">Financial<br>Engineering</div>
    <div class="table-cell">Ew.</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img class="square2" src="252.jpg" /></div>
    <div class="table-cell">MA252</div>
    <div class="table-cell">Algorithm Design<br>and Anal.</div>
    <div class="table-cell">Abdul Bari, everyone.</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img class="square2" src="224.png" /></div>
    <div class="table-cell">MA224</div>
    <div class="table-cell">Real Anal. and<br>Measure Theory</div>
    <div class="table-cell">Baby Rudin's as terse as they say</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img class="square2" src="252-unused.png" /></div>
    <div class="table-cell">MA251</div>
    <div class="table-cell">Data Structures</div>
    <div class="table-cell">Meh. But good lab.</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img class="square2" src="222.png" /></div>
    <div class="table-cell">MA222</div>
    <div class="table-cell">Abstract Algebra, Number Theory</div>
    <div class="table-cell">Ring around the rosie. Had fun.</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img class="square2" src="225.png" /></div>
    <div class="table-cell">MA225</div>
    <div class="table-cell">Probability Theory</div>
    <div class="table-cell">uwu can i haz qwant?</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img class="square" src="221.png" /></div>
    <div class="table-cell">MA221</div>
    <div class="table-cell">Discrete Math</div>
    <div class="table-cell">Very vintage. Had fun.</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img class="square" src="201.png" /></div>
    <div class="table-cell">MA201</div>
    <div class="table-cell">Complex Anal. and PDEs</div>
    <div class="table-cell">Tristan Needham told me all I'll remember.</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img class="square2" src="102.png" /></div>
    <div class="table-cell">MA102</div>
    <div class="table-cell">Linear Algebra and ODEs</div>
    <div class="table-cell">I thank Axler wholeheartedly.</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img src ="bash.png" class="square2"/></div>
    <div class="table-cell">MA101</div>
    <div class="table-cell">Real Anal. and Multivariate Calc</div>
    <div class="table-cell">You are crushed and born anew.</div>
  </div>
</div>


## Education

<div class="table-container">
<div class="table-row">
  <div class="table-cell"><strong>School</strong></div>
  <div class="table-cell"><strong>Name</strong></div>
  <div class="table-cell"><strong>Degree</strong></div>
  <div class="table-cell"><strong>Year</strong></div>
</div>

  <div class="table-row">
    <div class="table-cell"><img src ="iitg.png" class="square"/></div>
    <div class="table-cell">IIT Guwahati</div>
    <div class="table-cell">Mathematics and Computing, B.Tech</div>
    <div class="table-cell">2026</div>
  </div>
  <div class="table-row">
    <div class="table-cell"><img src ="ths.png" class="square2"/></div>
    <div class="table-cell">THS Rohini</div>
    <div class="table-cell">High School, CBSE</div>
    <div class="table-cell">2022</div>
  </div>
</div>



<!-- 
## Experience

| Icon                                    | Firm       | Role  | Details | Year |
|-----------------------------------------|------------|-------|---------|------|
| <img class="square" src="sfdc.png"/>    | Salesforce | Intern|         | 2025 |
| <img class="square" src="tifr.png"/>    | TIFR       | VSRP  |         | 2024 |


## Courses I took
(read: survived)

| Text | Code  | Name                                  | Remark!?                                    |
|------|-------|---------------------------------------|---------------------------------------------|
|      | MA411 | Differential Geometry                 | So pissed at morning labs.                  |
|      | MA641 | Operator Theory on Hilbert Spaces     | He's actually the best.                     |
|      | MA271 | Financial Engineering                 | Ew.                                         |
|      | MA252 | Algorithm Design and Anal.            | Meh.                                        |
|      | MA224 | Real Anal. and Measure Theory         | Tip my hat to Cantor.                       |
|      | MA251 | Data Structures                       | Meh. But good lab.                          |
|      | MA222 | Abstract Algebra, Number Theory       | Ring around the rosie. Had fun.             |
|      | MA225 | Probability Theory                    | uwu can i haz qwant?                        |
|      | MA221 | Discrete Math                         | Very vintage. Had fun.                      |
|      | MA201 | Complex Anal. and PDEs                | Tristan Needham told me all I remember.     |
|      | MA102 | Linear Algebra and ODEs               | I thank Axler wholeheartedly.               |
|      | MA101 | Real Anal. and Multivariate Calculus  | You are crushed and born anew.              |


## Education

|      | Name          | Degree                               | Year |
|------|---------------|--------------------------------------|------|
|      | IIT Guwahati  | Mathematics and Computing, B.Tech    | 2026 |
|      | THS Rohini    | High School, CBSE                    | 2022 |
-->
