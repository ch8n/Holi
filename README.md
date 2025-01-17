# Holi
### A library of colors, gradients and utils built using Jetpack Compose for Android

[![License MIT](https://img.shields.io/badge/Licence-MIT-blue.svg)](https://raw.githubusercontent.com/patilsiddhesh/Holi/main/LICENSE)
![Maven Central](https://img.shields.io/maven-central/v/com.siddroid/holi?label=Maven%20Central&style=flat-square)

### Features

* A wide collection of colors from different palettes for easy access in your pet projects
* Provides easy gradient building functions that all your composable brushes need
* Just 28 KB in size! Over 450 predefined colors and endless gradients.

### Color Palettes

* Material Colors
* Flat Colors
* Cool Colors
* Dracula Colors

## Color palette showcase

|                           Cool Colors                           |                         Material colors                         |                           Flat colors                           |                         Dracula colors                          |
| :-------------------------------------------------------------: | :-------------------------------------------------------------: | :-------------------------------------------------------------: | :-------------------------------------------------------------: |
| ![](https://media.giphy.com/media/S4uHXw9SoQaEl14b3c/giphy.gif) | ![](https://media.giphy.com/media/otyj84B8RncGPo6rxC/giphy.gif) | ![](https://media.giphy.com/media/NLnvrD57u5iJ2IbQGO/giphy.gif) | ![](https://media.giphy.com/media/CGbaGmKoym3rqsf7XQ/giphy.gif) |

### Gradient mixer showcase

|                      Directional Gradients                      |                Directional multi color gradients                |
| :-------------------------------------------------------------: | :-------------------------------------------------------------: |
| ![](https://media.giphy.com/media/d2ZAyZDFgFm5ZPX8v4/giphy.gif) | ![](https://media.giphy.com/media/80odY16jAXAuUCDyds/giphy.gif) |

### Using colors

You can simply pick colors by using the container objects for each palette and profit.

Eg.
```kotlin
   MaterialColor.RED
   CoolColor.FIREBRICK
   FlatColor.EMERLAND
   DraculaColor.YELLOW
```

![](https://media.giphy.com/media/CTRkESw2qqbuBLgR86/giphy.gif)

### Palette references

* [Material Colors](https://www.materialui.co/colors)
* [Flat Colors](https://www.materialui.co/flatuicolors)
* [Cool Colors](https://www.materialui.co/htmlcolors)
* [Dracula Colors](https://draculatheme.com/contribute/)


### Using Gradients

Using gradients is super easy with Holi, just use GradientMixer and choose from various gradient brush generating functions.

#### 1. Mixing two colors
```kotlin
   GradientMixer.bottomLeftToTopRight(MaterialColor.RED,MaterialColor.GREEN)
```

#### 2. Mixing more than two colors
```kotlin
   GradientMixer.topRightToBottomLeft(
    listOf(MaterialColor.RED,
    MaterialColor.GREEN,
    MaterialColor.PURPLE)
    )
```

#### 3. Reversing gradients
```kotlin
   GradientMixer.rightToLeft(FlatColor.CARROT,FlatColor.POMEGRANATE,reversed = true)
```

![](https://media.giphy.com/media/W5pC7NKZVsKcu7bEh8/giphy.gif)

Holi's GradientMixer is a container for gradient (Compose Brush) generating functions. These functions act as wrappers around Compose's gradient generators so that you don't have to figure out offset values with their directions.
The idea behind this gradient mixer is easy access to gradient building.

## How to use

Holi is available on MavenCentral, declare maven central in your repositories and implement the latest version in dependencies.

#### Step 1. Add to repositories

```groovy

allprojects {
    repositories {
        mavenCentral()
    }
}

```


#### Step 2. Add in dependencies

```groovy

dependencies {

    implementation 'com.siddroid:holi:0.0.7'

}

```

#### Step 3. (Optional) Setting up with local composition

Wrap your Material theme composable with `HoliPaletteComposition` to use colors through MaterialTheme object

Eg.
```kotlin
@Composable
fun HoliTheme(...) {
    ...

    HoliPaletteComposition {
        MaterialTheme(
            colors = colors,
            content = content
        )
    }

}

```
After this you can safely use

```kotlin
Text(
    text = "Holi Local Composition!",
    color = MaterialTheme.flatColors.CLOUDS
)
```

## Licensing

```
  MIT License

  Copyright (c) 2021 Siddhesh Patil, Siddroid.com

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, andor sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in all
  copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
  SOFTWARE.

```

## Disclaimer

Holi uses color palettes from the reference sites, these colors / swatches are free to use. A big thanks to the maintainers for making these color palettes.