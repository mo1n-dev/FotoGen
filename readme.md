# FotoGen

---

## What is this "FotoGen" about?

FotoGen is a web app to get random images every time, save those images as jpeg file and finally share the image to your social media if you like it

---

## Try FotoGen here ==> https://mo1n-dev.github.io/FotoGen/
---

## Visual status of FotoGen

<img width="684" alt="Screen Shot 2021-07-09 at 7 26 26 PM" src="https://user-images.githubusercontent.com/85831534/125116276-c9f34880-e0ec-11eb-832e-b84a75bc61a7.png">
### Fetch Api from Unsplash with JavaScript

```const numItemsToGenerate = 1;
 function renderItem() {
   fetch(`https://source.unsplash.com/920x720?beach`)
  .then(resp => resp.blob())
  .then(image => {
    const image_url = URL.createObjectURL(image)
    let item = document.getElementById('container');
    item.innerHTML = `<img class="beach_image" src="${image_url}" alt="beach image"/>`;
    return image_url;
  }).then(url=>document.querySelector(".download").onclick = ()=>downloadImage(url))
}

renderItem()


```

## HTML

```
<header class="head">
		<h1>Foto<span>Gen</span></h1>

	</header>


	<div class="main">
	<div id="container">
	</div>

	<div id="button">
		<button class="custom-btn btn-9" onclick="renderItem()">Get New</button>
		<button class="custom-btn btn-12 download"><span>Downloaded</span><span>Download</span></button>
		<button class="custom-btn btn-3"  onclick="tweetCurrentPage()"><span>Tweet</span></button>
	</div>
	<div class="footer_portion">
		<a href="#" target="_blank" class="facebook_two"><i class="fa fa-facebook"></i></a>
		<a href="#" target="_blank" class="twitter_two"><i class="fa fa-twitter"></i></a> <br><br>
		Recreated by Moinuddin Ahmad Shuvo<br><br>
		Copyright © 2018-2020. All rights reserved by BdGeeks
		</div>
```

## CSS

```
  @media (max-width) {
  .head {
    text-align: center;
  }
  #button {
    display: flex;
    flex-direction: column;
  }
  .footer_portion {
    display: flex;
    align-items: flex-end;
  }
  }
```

---

## Helpful resources

#### Images

- [Unsplash Random Images](https://source.unsplash.com/random)

#### Fonts

- [Google Fonts](https://fonts.google.com/)

#### HTML

- [Beginners Guide to HTML](https://www.codecademy.com/learn/learn-html)

#### CSS

- [Beginners Guide to CSS](https://www.codecademy.com/learn/learn-css)

---

## Sharing Project Experience!

The project was such a wonderful experience. It was challenging, meaningful, and deeply fulfilling✨
