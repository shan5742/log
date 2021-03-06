# JavaScript

Javascript has been my core focus since begin my journey into programming, I have a [repo for coding challenges](https://github.com/shan5742/codingchallenges) another following my progress through [eloquentJS](https://github.com/shan5742/eloquent-js) and I am thinking about starting another logging my progress through Wes Bos' JavaScript 30 course, but for now I think I will just leave one example of from the course below, to give an idea of the type of things I will be learning from it.

### JavaScript 30 

So far the course has been an amazing resource for learning vanilla JS. Most of the other projects from the course can be found as separate repo's in my [GitHub profile](https://github.com/shan5742/), but I figured this one could go in the log because it is not really about building anything and more about working with various array tools we have available to us in JS. Array Cardio helps improve our understanding of:

- **Filter**
- **Map**
- **Sort**
- **Reduce**

Oh and it also introduces us to `console.table`, which is awesome!!

## Array Cardio Day 1

### Some data we can work with

```
    const inventors = [
      { first: 'Albert', last: 'Einstein', year: 1879, passed: 1955 },
      { first: 'Isaac', last: 'Newton', year: 1643, passed: 1727 },
      { first: 'Galileo', last: 'Galilei', year: 1564, passed: 1642 },
      { first: 'Marie', last: 'Curie', year: 1867, passed: 1934 },
      { first: 'Johannes', last: 'Kepler', year: 1571, passed: 1630 },
      { first: 'Nicolaus', last: 'Copernicus', year: 1473, passed: 1543 },
      { first: 'Max', last: 'Planck', year: 1858, passed: 1947 },
      { first: 'Katherine', last: 'Blodgett', year: 1898, passed: 1979 },
      { first: 'Ada', last: 'Lovelace', year: 1815, passed: 1852 },
      { first: 'Sarah E.', last: 'Goode', year: 1855, passed: 1905 },
      { first: 'Lise', last: 'Meitner', year: 1878, passed: 1968 },
      { first: 'Hanna', last: 'Hammarström', year: 1829, passed: 1909 }
    ];
```

```
    const people = ['Beck, Glenn', 'Becker, Carl', 'Beckett, Samuel', 'Beddoes, Mick', 'Beecher, Henry', 'Beethoven, Ludwig', 'Begin, Menachem', 'Belloc, Hilaire', 'Bellow, Saul', 'Benchley, Robert', 'Benenson, Peter', 'Ben-Gurion, David', 'Benjamin, Walter', 'Benn, Tony', 'Bennington, Chester', 'Benson, Leana', 'Bent, Silas', 'Bentsen, Lloyd', 'Berger, Ric', 'Bergman, Ingmar', 'Berio, Luciano', 'Berle, Milton', 'Berlin, Irving', 'Berne, Eric', 'Bernhard, Sandra', 'Berra, Yogi', 'Berry, Halle', 'Berry, Wendell', 'Bethea, Erin', 'Bevan, Aneurin', 'Bevel, Ken', 'Biden, Joseph', 'Bierce, Ambrose', 'Biko, Steve', 'Billings, Josh', 'Biondo, Frank', 'Birrell, Augustine', 'Black Elk', 'Blair, Robert', 'Blair, Tony', 'Blake, William'];
```

#### Array.prototype.filter()

**Filter the list of inventors for those who were born in the 1500's**

```
    const fifteen = inventors.filter(inventor => (inventor.year >= 1500 && inventor.year < 1600));
    console.table(fifteen);
```

#### Array.prototype.map()

**Give us an array of the inventor first and last names**

```
    const fullNames = inventors.map(inventor => `${inventor.first} ${inventor.last}`);
    console.log(fullNames);
```

#### Array.prototype.sort()

**Sort the inventors by birthdate, oldest to youngest**

```
    const ordered = inventors.sort((a, b) => a.year > b.year ? 1 : -1);
    console.table(ordered);
```

#### Array.prototype.reduce()

**How many years did all the inventors live?**

```
    const totalYears = inventors.reduce((total, inventor) => {
      return total + (inventor.passed - inventor.year);
    }, 0);
    console.log(totalYears);
```
### Additional Exercises

**Sort the inventors by years lived**

```
    const oldest = inventors.sort(function(a, b) {
      const lastInventor = a.passed - a.year;
      const nextInventor = b.passed - b.year;
      return lastInventor > nextInventor ? -1 : 1;
    });
    console.table(oldest);
```

**Create a list of Boulevards in Paris that contain 'de' anywhere in the name**

*https://en.wikipedia.org/wiki/Category:Boulevards_in_Paris*

 ```
     const category = document.querySelector('.mw-category');
     const links = Array.from(category.querySelectorAll('a'));
     const de = links
                 .map(link => link.textContent)
                .filter(streetName => streetName.includes('de'));
```

#### Sort Exercise

**Sort the people alphabetically by last name**

```
    const alpha = people.sort((lastOne, nextOne) => {
      const [aLast, aFirst] = lastOne.split(', ');
      const [bLast, bFirst] = nextOne.split(', ');
      return aLast > bLast ? 1 : -1;
    });
    console.log(alpha);
```

#### Reduce Exercise

**Sum up the instances of each of these**

```
    const data = ['car', 'car', 'truck', 'truck', 'bike', 'walk', 'car', 'van', 'bike', 'walk', 'car', 'van', 'car', 'truck', 'pogostick'];
    const transportation = data.reduce(function(obj, item) {
      if (!obj[item]) {
        obj[item] = 0;
      }
      obj[item]++;
      return obj;
    }, {});
    console.log(transportation);
```