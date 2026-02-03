# td-shadertoy-minimal

## Overview

This is a fork of https://github.com/matthewwachter/td-shadertoy with the following changes

- Subnetwork is vastly simplified. Everything is visible as soon as you dive into the network, making it easy to inspect and change the generated GLSL workflow (or configure uniforms)
- It overcomes the Shadertoy API restrictions by using a human-in-the-loop. Basically, Shadertoy API is no longer usable from scripts because it issues you a Cloudflare Captcha / Javascript challenge. To get around this, we prompt the user to enter the URL in their browser and copy-paste the JSON into TD

## Usage

1. Add the tox into your project
2. Go to a shadertoy project e.g. [https://www.shadertoy.com/view/tsScRK]([url](https://www.shadertoy.com/view/tsScRK)), copy the identifier at the end `tsScRK`
3. Paste it into the `ShaderID` param in TD, press "Update URL"
4. Open the URL in your browser, you'll see a bunch of JSON
5. Copy ALL of the json and paste it into the "Data" param in TD
6. Press "Load"

## Notes

- This doesn't work with all TD Shaders, some will have GLSL errors. If you want to improve the project, contributions are welcome.
- Not all shaders are accessible via API. There's a hack where you can fork the project then change the visibility to Public + API. However this is considered bad form on ShaderToy. Be a nice person and delete your fork after you've imported it into TD.
