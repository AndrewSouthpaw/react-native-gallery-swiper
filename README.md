<a href="https://luehangs.site"><img src="https://luehangs.site/images/react-native-gallery-swiper-main.jpg" alt="react-native-gallery-swiper"/></a>

> An easy and simple to use React Native component to render an image gallery with common gestures like pan, pinch and double tap.  Supporting both iOS and Android. Free and made possible along with costly maintenance and updates by [Lue Hang](https://www.facebook.com/lue.hang) (the author).

<a href="https://luehangs.site"><img src="https://luehangs.site/images/lh-blog-strip.jpg" alt="LH BLOG"/></a>

![react-native-gallery-swiper](https://www.luehangs.site/videos/react-native-gallery-swiper-demo.gif)

Learn more about React Native with project examples along with Cyber Security and Ethical Hacking at [LH BLOG](https://www.luehangs.site).

## Index

- [Install](#install)
- [Usage Example](#usage-example)
- [API](#api)
- [Props](#props)
- [Scroll State and Events](#scroll-state-and-events)
- [Example Project](#example-project)
- [Contribute](#contribute)
- [License](#license)

Improved and changed on top of `react-native-image-gallery`.

## Install

Type in the following to the command line to install the dependency.

```bash
$ npm install --save react-native-gallery-swiper
```

or

```bash
$ yarn add react-native-gallery-swiper
```

## Usage Example

Add an ``import`` to the top of the file.  At minimal, declare the ``GallerySwiper`` component in the ``render()`` method providing an array of data for the ``images`` prop.

```javascript
import GallerySwiper from "react-native-gallery-swiper";

//...
render() {
    return (
        <GallerySwiper
            style={{ flex: 1, backgroundColor: "black" }}
            images={[
                // Version *1.1.0 update (or greater versions): 
                // Can be used with different image object fieldnames.
                // Ex. source, source.uri, uri, URI, url, URL
                { uri: "https://luehangs.site/pic-chat-app-images/beautiful-blond-blonde-hair-478544.jpg" },
                { source: require("yourApp/image.png"), dimensions: { width: 1080, height: 1920 } },
                { source: { uri: "https://luehangs.site/pic-chat-app-images/beautiful-beautiful-women-beauty-40901.jpg" } },
                { uri: "https://luehangs.site/pic-chat-app-images/animals-avian-beach-760984.jpg",
                    dimensions: { width: 1080, height: 1920 } },
                { URI: "https://luehangs.site/pic-chat-app-images/beautiful-blond-fishnet-stockings-48134.jpg" },
                { url: "https://luehangs.site/pic-chat-app-images/beautiful-beautiful-woman-beauty-9763.jpg" },
                { URL: "https://luehangs.site/pic-chat-app-images/attractive-balance-beautiful-186263.jpg" },
            ]}
        />
    );
}
//...
```

<a href="https://luehangs.site"><img src="https://luehangs.site/images/lh-blog-strip.jpg" alt="LH BLOG"/></a>

## API

``<GallerySwiper />`` component accepts the following props...

## Props

Props | Description | Type | Default
------ | ------ | ------ | ------
`images` | An array of objects.  `source`, `source.uri`, `uri`, `URI`, `url` or `URL` is a required field (if multiple similar fields in an image object, priority will go from start `source` to last `URL`). EX. `[{ source: require("yourApp/image.png"), dimensions: { width: 1080, height: 1920 } }, { uri: "https://luehangs.site/pic-chat-app-images/animals-avian-beach-760984.jpg", dimensions: { width: 1080, height: 1920 } }, { uri: "https://luehangs.site/pic-chat-app-images/beautiful-blond-blonde-hair-478544.jpg"}]` | `Array` | Required
`initialPage` | Index of image to be displayed first. | `number` | `0`
`imageComponent` | Custom function to render your images. 1st param is the **image props** and 2nd is its **dimensions**. | `Function` | `<Image/>` component
`errorComponent` | Custom function to render the page of an image that couldn't be displayed. | `Function` | A `<View/>` with a stylized error
`flatListProps` | Props to be passed to the underlying `FlatList`. | `Object` | `{windowSize: 3}`
`pageMargin` | Blank margin space to show between images. | `number` | `0`
`onPageSelected` | Fired with the index of page that has been selected. | `Function`
`onPageScrollStateChanged` | Called when page scrolling state has changed, see [scroll state and events](#scroll-state-and-events). | `Function`
`onPageScroll` | Scroll event, see [scroll state and events](#scroll-state-and-events). | `Function`
`scrollViewStyle` | Custom style for the `FlatList` component. | `Object` | `{}`
`onSingleTapConfirmed` | Executed after a single tap. | `Function`
`onLongPress` | Executed after a long press. | `Function`

<a href="https://luehangs.site"><img src="https://luehangs.site/images/lh-blog-strip.jpg" alt="LH BLOG"/></a>

## Scroll state and events

* `onPageScroll` : (event) => {}. 

    The event object carries following data: 

    * `position`:  index of first page from the left that is currently visible.
    * `offset`: value from range [0,1) describing stage between page transitions.
    * `fraction`: means that (1 - x) fraction of the page at "position" index is visible, and x fraction of the next page is visible.

* `onPageScrollStateChanged` : (state) => {}.

    Called when the page scrolling state has changed. The page scrolling state can be in 3 states:

    * `'idle'`: there is no interaction with the page scroller happening at the time.
    * `'dragging'`: there is currently an interaction with the page scroller.
    * `'settling'`: there was an interaction with the page scroller, and the page scroller is now finishing its closing or opening animation.

## Example Project

Perform steps 1-2 to run locally:

1. [Clone the Repo](#1-clone-the-repo)
2. [Install and Run](#2-install-and-run)

### 1. Clone the Repo

**Clone** `react-native-gallery-swiper` locally. In a terminal, run:

```bash
$ git clone https://github.com/Luehang/react-native-gallery-swiper.git react-native-gallery-swiper
```

### 2. Install and Run

```bash
$ cd react-native-gallery-swiper/example/
```

#### iOS - Mac - Install & Run

	1. check out the code
	2. npm install
	3. npm run ios

#### Android - Mac - Install & Run

	1. check out the code
	2. npm install
	3. emulator running in separate terminal
	4. npm run android

<a href="https://luehangs.site"><img src="https://luehangs.site/images/lh-blog-strip.jpg" alt="LH BLOG"/></a>

## Contribute

[Pull requests](https://github.com/Luehang/react-native-gallery-swiper/pulls) are welcomed.

### Beginners

Not sure where to start, or a beginner? Take a look at the [issues page](https://github.com/Luehang/react-native-gallery-swiper/issues).

### Author

<a href="https://www.facebook.com/lue.hang">
<img src="https://www.luehangs.site/images/lue-hang2018-circle-150px.png"/>
</a>

Free and made possible along with costly maintenance and updates by [Lue Hang](https://www.facebook.com/lue.hang) (the author).

### Contributors

Contributors will be posted here.

## License

MIT © [Lue Hang](https://luehangs.site), as found in the LICENSE file.
