## Testimonials Video Slider WordPress

:white_check_mark: PHP version >= 7.2    
:white_check_mark: Wordpress - 6.1.1   
:white_check_mark: Slider - [SplideJs, v4](https://splidejs.com/)    
____

The plugin must be installed in the WordPress directory `/wp-content/plugins/`.    
In the plugin directory, create a folder `custom-testimonials-slider` and place the plugin files in it.    
It should be like this: `/wp-content/plugins/custom-testimonials-slider/`.    

Additionally, you need to install plugin [Advanced Custom Fields](https://www.advancedcustomfields.com/) and create the following fields:    

:small_blue_diamond: `client_name` (field type Text)    
:small_orange_diamond: `client_position` (field type Text)    
:small_blue_diamond: `text_testimonials` (field type Text)    
:small_orange_diamond: `link_video` (field type Text Url)    

*According to the [slider documentation](https://splidejs.com/extensions/video/) to assign videos to slides use data attribute, that's why in ACF it is implemented via Field type URL instead of oembed.*        

If you want to create multiple sliders, you need to add the `data-splide` attribute to your slider's html code.   
For example,    
```html
      <div class="splide" data-splide='{"type":"loop","perPage":3, "arrows":false, "pagination":false, "heightRatio":0.25 }'>
         <div class="splide__track">
            <ul class="splide__list">
            <li class="splide__slide">
               <img src="https://lorempixel.com/400/200/food/" class="slider-img">
            </li>
            <li class="splide__slide">
               <img src="https://lorempixel.com/400/200/food/2" class="slider-img">
            </li>
            <li class="splide__slide">
               <img src="https://lorempixel.com/400/200/food/3" class="slider-img">
            </li>
            <li class="splide__slide">
               <img src="https://lorempixel.com/400/200/food/4" class="slider-img">
            </li>
            <li class="splide__slide">
               <img src="https://lorempixel.com/400/200/food/5" class="slider-img">
            </li>
            </ul>
         </div>
      </div>
```
See [documentation](https://splidejs.com/guides/options/#by-data-attribute)

In the Testimonials menu of the admin panel, you need to create slides and fill out these fields.        

![Screenshort](/img/screen_slider.png)

To display a picture of a slide, you need to add a thumbnail of the post.    

[View slider](https://nastmobile.com/web-test/slider-example/)
