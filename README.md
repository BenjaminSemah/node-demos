# Shotstack Node Examples

### Video examples

- **text.js** -
    Create a HELLO WORLD video title against black background with a zoom in motion effect and soundtrack.

- **images.js** -
    Takes an array of image URLs and creates a video with a soundtrack and simple zoom in effect.

- **titles.js** -
    Create a video to demo titles using the available preset font styles, a soundtrack, zoom in motion effect and 
    wipe right transition.

- **trim.js** -
    Trim the start and end of a video clip to output a shortened video.

- **filters.js** -
    Applies filters to a video clip, including a title with the name of the filter and a soundtrack.

- **picture-in-picture.js** -
    Layer a small foreground clip, using position and scale, over a fullscreen background clip, to create a picture 
    in picture effect.

- **merge.js** -
    Merge data in to a video using merge fields.

- **merge-trim.js** -
    Trim a video using merge fields. Replace the URL, trim and length using placeholders and merge field values.

- **transform.js** -
    Apply transformations (rotate, skew and flip) to a video clip.

- **progress.js** -
    Animate and overlay a progress bar on to a video using an HTML asset.

- **frames.js** -
    A frame accurate counter, useful for testing frame accuracy.

- **countdown.js** -
    A simple 10 second countdown video, variables can be adjusted to created different speeds and counts.
    
### Image examples

- **border.js** -
    Add a border frame around a background photo.

- **gif.js** -
    Create an animated gif that plays once.

### Template examples

- **templates/create.js**
    Save an edit as a re-usable template with placeholders.

- **templates/render.js**
    Render a template using merge fields to replace placeholders.

- **templates/templates.js**
    Get a list of all templates.

- **templates/templates.js**
    Get an individual template by template ID.

### Polling example

- **status.js** -
    Shows the status of a render task and the output video URL. Run this after running one of the render examples.

### Probe example

- **probe.js** -
    Fetch metadata for any media asset on the internet such as width, height, duration, etc...

### Asset management examples

- **serve-api/renderId.js** -
    Fetch all assets associated with a render ID. Includes video or image and thumbnail and poster.

- **serve-api/assetId.js** -
    Fetch an individual asset by asset ID.

- **destination.js** -
    Shows how to exclude a render from being sent to the Shotstack hosting destination.

- **mux.js** -
    Sends a rendered video to Mux hosting and excludes it from Shotstack. Requires a Mux account.

- **s3.js** -
    Sends a rendered video to an AWS S3 bucket and excludes it from Shotstack. Requires an AWS account and correctly
    configured bucket (see: https://community.shotstack.io/t/s3-permission-issue/397).

### Installation

Install the required dependencies including the [Shotstack Node SDK](https://www.npmjs.com/package/shotstack-sdk)

```bash
npm install
```

### Set your API key

The demos use the **staging** endpoint by default so use your provided **staging** key:

```bash
export SHOTSTACK_KEY=your_key_here
```

Windows users (Command Prompt):

```bash
set SHOTSTACK_KEY=your_key_here
```

You can [get an API key](http://shotstack.io/?utm_source=github&utm_medium=demos&utm_campaign=node_sdk) via the 
Shotstack web site.

### Run an example

The examples directory includes a number of examples demonstrating the capabilities of the 
Shotstack API.

#### Rendering

To run a rendering/editing example run the examples at the root of the examples folder, e.g. to run the images video 
example:

```bash
node examples/images.js
```

#### Polling

To check the status of a render, similar to polling run the `status.js` example with the render ID, e.g.:

```bash
node examples/status.js 8b844085-779c-4c3a-b52f-d79deca2a960
```

#### Asset management

To look up assets hosted by Shotstack run the examples in the [examples/serve-api](./examples/serve-api/) directory.

Find assets by render ID:
```bash
node examples/serve-api/renderId.js 8b844085-779c-4c3a-b52f-d79deca2a960
```

or 

Find an asset by asset ID:
```bash
node examples/serve-api/assetId.js 3f446298-779c-8c8c-f253-900c1627b776
```
