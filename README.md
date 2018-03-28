## The Problem
As we enter an age that is progressively more defined by artificial intelligence and machine learning, we must come to terms with some of their limitations. The past few years have been rife with news about racial biases within AI algorithms. One of the primary problems with AI today is how it can manifest inherent human biases in actual applications. As more of these errors occur, they will only serve to further disenfranchise specific groups within our society. 

## Our Solution
Most solutions to this problem usually deal with completely retooling individual AI algorithms to reduce bias. This is a very inefficient and resource-heavy approach for most companies. Our solution is to have an image/video preprocessor that normalizes faces before they are analyzed by AI. This allows our product to be easily injected and implemented into existing software stacks as a single discrete step. 

## How we built it
We used constrained local models fitted by regularized landmark mean-shift to fit facial models to faces in videos. By tracking individual feature points, we were able to overlay a face-normalization mask over the video. This mask allows us to provide race/sex/age-agnostic expressions and responses to existing AI algorithms.

## Challenges we ran into
Initially, we drew a lot of inspiration from the deepfakes faceswapping algorithm. We tried to set up the model and train it using Google Cloud Platform, but ran into several building issues, which led our training time to exceed the scope of the hackathon. We transitioned to a Javascript approach fairly late, which resulted in a somewhat glitchy demo.

## What's next for Face Normalizer
Moving forward, we want to use more accurate face tracking techniques to our masking layer to reduce glitches and improve performance. 

## Development

First, install [node.js](http://nodejs.org/) with npm.

In the root directory of clmtrackr, run `npm install` then run `npm run build`. This will create `clmtrackr.js` and `clmtrackr.module.js` in `build` folder.

To test the examples locally, you need to run a local server. One easy way to do this is to install `http-server`, a small node.js utility: `npm install -g http-server`. Then run `http-server` in the root of clmtrackr and go to `https://localhost:8080/examples` in your browser.