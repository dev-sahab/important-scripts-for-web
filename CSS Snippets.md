## Important CSS Snippets

![Screenshot](https://www.tutorialrepublic.com/lib/images/css-illustration.png)
#

### Increase First Letter Font Size 

```css

/* first letter css */

selector::first-letter {
    display: inline-block;
    margin-right: 5px;
    line-height: 0.8;
    float: left;
    clear: both;
    font-family: 'Playfair Display', serif;
    font-size: 60px;
    color: #ff5740;
}

```
#### Example
![screenshot](https://github.com/shb-services/imortant-scripts-for-web/blob/main/assets/First%20Letter.png)

#

```css
selector .elementor-widget-container::before {
    position: absolute;
    top: 0;
    left: -100%;
    display: block;
    content: '';
    width: 50%;
    height: 100%;
    background: linear-gradient(to right, rgba(255, 255, 255, 0) 0%, rgba(255, 255, 255, .3) 100%);
    transform: skewX(-25deg);
    z-index: 2;
}

selector .elementor-widget-container:hover::before{
    -webkit-animation: slide 1.3s;
    animation: slide 1.3s;

}

@keyframes slide {
    0% {
        left: -100%;
    }
    100% {
        left: 125%;
    }
}
```
