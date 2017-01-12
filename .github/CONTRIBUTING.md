## Contributing
I'm very open to contributions, big and small! For general instructions on contributing to a project on Github, see this guide: [Fork A Repo](https://help.github.com/articles/fork-a-repo).

You will need to install [npm](https://www.npmjs.org) to build the project. You will also need [evenizer](https://github.com/katapad/evenizer) (`npm install -g evenizer`) and [imagemagick](http://www.imagemagick.org/) to generate retina flag sprites. Then run `npm install` to install Grunt and other dependencies, then you should be good to run `grunt build` to build the project. At this point, the included demo.html should be working. You should make your changes in the `src` directory and be sure to run `grunt build` again before committing.

Running `grunt build` can be quite slow - you can also run `grunt js` to just build the JavaScript, and `grunt jasmine` to just run the tests.

If when building, you get an error in the "exec:evenizer" task, you may need to temporarily increase the ulimit by running this command: `ulimit -S -n 2048`

I came up with below issue when doing `grunt build` in windows

`[Error: Could not execute GraphicsMagick/ImageMagick: identify "-ping" "-verbose" "your path" this most likely means the gm/convert binaries can't be found]`

I have got it resolved by installing graphicsmagick and imagemagick and its path in environment variable will be automatically set up. Then I have to restart the windows to reflect the changes and now I can successfully converts and image.I found this in below link

http://stackoverflow.com/questions/31214724/gm-conversion-issue-in-node-js

after this I got evenizer error, I got this fixed by installing evenizer as mentioned above.

Installation for ubuntu 14.04

https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions

link to install imagemagick in ubuntu 14.04

https://www.enovate.co.uk/blog/2015/12/16/how-to-install-imagemagick-from-source-on-ubuntu-14.04
