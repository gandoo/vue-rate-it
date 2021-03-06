<template>
    <div class="ui basic segment" style="font-size:1.1em;">
        <h1 class="ui header">Image Rating Component</h1>
        <div class="ui divider"></div>
        <p>The image rating component allows you to use any image as a rater. Because of the nature of images this component features different customisation options to the pure SVG components.</p>

        <image-rating src="images/vueLogo.png"></image-rating>

        <div class="ui segment">
            <!-- HTML generated using hilite.me -->
            <div style="background: #ffffff; overflow:auto;width:auto;;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #1e90ff; font-weight: bold">&lt;image</span><span style="color: #1e90ff">-rating</span> <span style="color: #1e90ff">src=</span><span style="color: #aa5500">&quot;/images/vueLogo.png&quot;</span><span style="color: #1e90ff; font-weight: bold">&gt;</span><span style="color: #1e90ff; ">&lt;/image-rating&gt;</span>
</pre></div>
        </div>

        <h1 class="ui header">Setup</h1>
        <div class="ui divider"></div>
        The image rating component can either be included via NPM (recommended) or CDN.

        <h2 class="ui header">NPM</h2>
        <p>Using the image-rating component via NPM is simple, once vue-rate-it has been installed you simply need to import it into your component:</p>

        <div class="ui segment">
            <!-- HTML generated using hilite.me -->
            <div style="background: #ffffff; overflow:auto;width:auto;;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #0000aa">import</span> {Image} from <span style="color: #aa5500">&#39;vue-rate-it&#39;</span>;

<span style="color: #0000aa">export</span> <span style="color: #0000aa">default</span>{
  components:{
   ImageRating
  } 
}
</pre></div>

        </div>

        <h2 class="ui header">CDN</h2>
        <p>You may also include the image-rating component via unpkg by adding the following to your page:</p>

        <div class="ui segment">
            <!-- HTML generated using hilite.me -->
            <div style="background: #ffffff; overflow:auto;width:auto;;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #1e90ff; font-weight: bold">&lt;link</span> <span style="color: #1e90ff">rel=</span><span style="color: #aa5500">&quot;stylesheet&quot;</span> <span style="color: #1e90ff">href=</span><span style="color: #aa5500">&quot;https://unpkg.com/vue-rate-it/dist/image-rating.min.js&quot;</span><span style="color: #1e90ff; font-weight: bold">&gt;</span>
</pre></div>
        </div>

        <p>It is automatically registered so there is no need to do anything else.</p>

        <h1 class="ui header">Documentation</h1>
        <div class="ui divider"></div>

        <h2 class="ui header">Props</h2>

        <p>The image rating component includes the following props:</p>
        <table class="ui celled table">
            <thead>
                <tr>
                    <th>Prop</th>
                    <th>Type</th>
                    <th>Description</th>
                    <th>Default</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>src</td>
                    <td>String</td>
                    <td>The url of the image you want to use for your rating items. (<b>Required</b>)</td>
                    <td>null</td>
                </tr>
                <tr>
                    <td>increment</td>
                    <td>Number</td>
                    <td>The rating increment. For example pass 0.5 for half rating or 0.01 for fluid ratings. Expects a number between 0.01 - 1.</td>
                    <td>1</td>
                </tr>
                <tr>
                    <td>rating</td>
                    <td>Number</td>
                    <td>
                        <p>The initial rating. This will automatically round to the closest increment, so for the most accurate rating pass 0.01 as increment. </p>
                        <div class="ui warning message" style="font-size:0.9em;">
                            In Vue 2.2 and above you can use <b>v-model</b> instead of "rating" to automatically sync values between the parent and child. </div>
                    </td>

                    <td>0</td>
                </tr>
                <tr>
                    <td>max-rating</td>
                    <td>Number</td>
                    <td>The maximum rating, this lets vue-rate-it know how many images to display.</td>
                    <td>5</td>
                </tr>
                <tr>
                    <td>background-opacity</td>
                    <td>Number</td>
                    <td>The opacity of the non-highlighted portion of a image. Expects a value between 0-1</td>
                    <td>0.02</td>
                </tr>

                <tr>
                    <td>item-size</td>
                    <td>Number</td>
                    <td>The size of each image. This gets passed to the SVG width attribute, so larger numbers are larger images.</td>
                    <td>50</td>
                </tr>
                <tr>
                    <td>show-rating</td>
                    <td>Boolean</td>
                    <td>Whether or not to show the rating next to the images.</td>
                    <td>true</td>
                </tr>
                <tr>
                    <td>read-only</td>
                    <td>Boolean</td>
                    <td>When set to true, the rater cannot be edited. Use in conjuction with increment to define rounding precision.</td>
                    <td>false</td>
                </tr>
                <tr>
                    <td>text-class</td>
                    <td>String</td>
                    <td>A css class name to style the rating text for a specific image rating component</td>
                    <td>""</td>
                </tr>
                <tr>
                    <td>fixed-points</td>
                    <td>Number</td>
                    <td>Specify the number of decimal points to display for the rating. If left blank the number of decimal points will be variable based by the current rating.</td>
                    <td>null</td>
                </tr>
                <tr>
                    <td>inline</td>
                    <td>Boolean</td>
                    <td>Sets the image rating to display inline.</td>
                    <td>false</td>
                </tr>
                <tr>
                    <td>spacing</td>
                    <td>Number</td>
                    <td>Sets the spacing between each image. This should be set as an offset, so minus figures move images closer together and plus figures move them further apart.</td>
                    <td>0</td>
                </tr>
            </tbody>
        </table>

        <h3 class="ui header">Props Example</h3>
        <p>The following is an example of a customised image-rating component:</p>

        <image-rating src="images/vueLogo.png" :item-size="40" v-model="rating" :increment="0.01"></image-rating>

        <div class="ui segment">
            <!-- HTML generated using hilite.me -->
            <div style="background: #ffffff; overflow:auto;width:auto;;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #1e90ff; font-weight: bold">&lt;image</span><span style="color: #1e90ff">-rating</span> <span style="color: #1e90ff">src=</span><span style="color: #aa5500">&quot;/images/vueLogo.png&quot;</span> 
              <span style="color: #1e90ff">:item-size=</span><span style="color: #aa5500">&quot;40&quot;</span>
              <span style="color: #1e90ff">:increment=</span><span style="color: #aa5500">&quot;0.01&quot;</span>
              <span style="color: #1e90ff">v-model=</span><span style="color: #aa5500">&quot;rating&quot;</span> <span style="color: #1e90ff; font-weight: bold">&gt;</span>
<span style="color: #1e90ff;">&lt;/image-rating&gt;</span>
</pre></div>

        </div>

        <div class="ui warning message" style="font-size:0.9em;">
            <div class="header">Using v-bind</div>
            <p>Vue requires that you pass Numbers and Boolean values using v-bind or the colon (:) shorthand as seen above.</p>
        </div>

        <h2 class="ui header">Custom Events</h2>
        <p>vue-rate-it emits the following events:</p>

        <table class="ui celled table">
            <thead>
                <tr>
                    <th>Event</th>
                    <th>Returns</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>rating-selected</td>
                    <td>Number</td>
                    <td>Returns the rating that the user has selected.</td>
                </tr>
                <tr>
                    <td>current-rating</td>
                    <td>Number</td>
                    <td>Returns the rating the mouse is currently over.</td>
                </tr>
            </tbody>
        </table>
        <div class="ui warning message" style="font-size:0.9em;">
            In Vue 2.2 and above you can use <b>v-model</b> instead of listening for the 'rating-selected' event to automatically sync values between the parent and child. </div>

        <h3 class="ui header">Custom Events Example</h3>
        <p>The following example shows how to use the "rating-selected" custom event to sync values and is the equivelent to using "v-model" which is only available when using Vue 2.2 and above</p>

        <div class="ui segment">
            <!-- HTML generated using hilite.me -->
            <div style="background: #ffffff; overflow:auto;width:auto;;border-width:.1em .1em .1em .8em;padding:.2em .6em;"><pre style="margin: 0; line-height: 125%"><span style="color: #1e90ff; font-weight: bold">&lt;image</span><span style="color: #1e90ff">-rating</span> <span style="color: #1e90ff;">@</span><span style="color: #1e90ff">rating-selected=</span><span style="color: #aa5500">&quot;rating = $event&quot;</span> <span style="color: #1e90ff">:rating=</span><span style="color: #aa5500">&quot;rating&quot;</span><span style="color: #1e90ff; font-weight: bold">&gt;</span><span style="color: #1e90ff;">&lt;/image-rating&gt;</span>
</pre></div>
        </div>

        <div class="ui warning message" style="font-size:0.9em;">
            When writing methods to capture custom events, the rating param is automatically passed to the method, so you can simply do:
            <br /><span style="font-family:courier;">&lt;image-rating @rating-selected="myMethod"&gt;&lt;/image-rating&gt;</span>
            <br /> If you need to declare methods with multiple paramaters you will need to use $event to pass the rating to the method:
            <br /><span style="font-family:courier;">&lt;image-rating @rating-selected="myMethod($event, anotherParam)"&gt;&lt;/image-rating&gt;</span></div>

        <h2 class="ui header">Image Sizing and Aspect Ration</h2>
        <p>The image-rating component automatically calculates image dimensions to maintain aspect ratio, below you can see that using a different image does not result in any distortion:</p>

        <image-rating src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Diet-Coke-Can.jpg" :increment="0.01"></image-rating>
        <p>Source: <a href="https://upload.wikimedia.org/wikipedia/commons/3/3c/Diet-Coke-Can.jpg">https://upload.wikimedia.org/wikipedia/commons/3/3c/Diet-Coke-Can.jpg</a></p>

        <div class="ui warning message">When using images on a transparent background with a small increment, you should try to minimise borders so it appears that the entire image represents one entire rating value. You can adjust the distance between images using the "spacing" prop.</div>
    </div>
</template>

<script type="text/javascript">
import {
    ImageRating
} from '../../../../src/index.js';
export default {
    components: {
        ImageRating
    },
    data() {
        return {
            rating: 3.5
        }
    }
}
</script>
