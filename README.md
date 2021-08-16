[![Contributors][contributors-shield]][contributors-url]
[![Languages][languages-shield]][languages-url]
[![Forks][forks-shield]][forks-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]


<!-- PROJECT LOGO & HEADER -->
<br />
<p align="center">

  <h3 align="center">Deto No Yoru</h3>

  <p align="center">
   Make date nights easier with Deto No Yoru!
    <br />
    <br />
    <a href="https://github.com/alynapchuk/detonoyoru/issues">Report Bug or Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

デートの夜 (Deto No Yoru) is a small website dedicated to making date nights easier. If you’re tired of never knowing what to watch or eat, Deto No Yoru is your solution! With the click of one button, our app will tell you which local restaurant you should try and what anime you should watch. If you’re still unsure of what to watch, our trending page will show you the top anime series according to MyAnimeList.

Each member of our team had been in a situation where hours had been spent debating with their significant other or friends over what to watch and what to eat. We set out to create a solution to end those painful hours scrolling through Netflix or Google maps. Rather than using an API based on recipes, it was important to our team that Deto No Yoru would be an easy date night fix by using local restaurants. By generating a random restaurant and anime, our goal was to take the “thinking” out of date night planning.


[![Product Name Screen Shot][product-screenshot]](https://example.com)

### Built With

* [HTML](#)
* [CSS](#)
* [JavaScript](#)

## APIs Used
* [Documenu](https://documenu.com/)
* [Jikan](https://jikan.docs.apiary.io/#) 

## Code Example
The following code uses the user-selected genre to fetch information from the jikan API. The array from the selected genre is then randomized. This same pattern was also used to fetch the random local restaurant.
``` javascript
    function fetchAnime(genre) {
        fetch(`https://api.jikan.moe/v3/genre/anime/${genre}`)
            .then(function (response) {
                return response.json();
            })
            .then(function (animeList) {
                randomizeAnime(animeList)

            })
            .catch(function (error) {
                console.error("ERROR: ", error);
            })
    }

    function randomizeAnime(animeList) {
        const randomAnime = Math.floor(Math.random() * animeList.anime.length);
```

<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/alynapchuk/detonoyoru/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Branch (`git checkout -b yourbranch/Contribution`)
3. Commit your Changes (`git commit -m 'added amazing feature'`)
4. Push to the Branch (`git push origin yourbranch/Contribution`)
5. Open a Pull Request



<!-- CONTACT -->
## Contact
Alyna Palamarchuk - [Portfolio](https://alynapchuk.com) - alynapchuk@gmail.com



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
[GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet) - [Img Shields](https://shields.io) - [Choose an Open Source License](https://choosealicense.com) - [GitHub Pages](https://pages.github.com) - [Animate.css](https://daneden.github.io/animate.css) - [Loaders.css](https://connoratherton.com/loaders) - [Slick Carousel](https://kenwheeler.github.io/slick) - [Smooth Scroll](https://github.com/cferdinandi/smooth-scroll) - [Sticky Kit](http://leafo.net/sticky-kit) - [JVectorMap](http://jvectormap.com) - [Font Awesome](https://fontawesome.com)





<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/alynapchuk/detonoyoru?color=219ebc&style=for-the-badge
[contributors-url]: https://github.com/alynapchuk/detonoyoru/graphs/contributors

[languages-shield]: https://img.shields.io/github/languages/count/alynapchuk/detonoyoru?color=90ab60&style=for-the-badge
[languages-url]: #

[forks-shield]: https://img.shields.io/github/forks/alynapchuk/detonoyoru?color=f5af00&style=for-the-badge
[forks-url]: #

[issues-shield]: https://img.shields.io/bitbucket/issues-raw/alynapchuk/detonoyoru?style=for-the-badge
[issues-url]: #

[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/alynapchuk/

[product-screenshot]: imgs/homepage.gif
