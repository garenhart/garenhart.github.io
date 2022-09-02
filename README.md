# garenhart.github.io
stoic.garenhart.com website

using remote jekyll theme: https://github.com/mmistakes/minimal-mistakes/

Following YouTube videos were instrumental in developing this website repo:
https://www.youtube.com/watch?v=NMmfYJZCHO4&list=WL&index=7&t=0s
https://www.youtube.com/watch?v=qWrcgHwSG8M

To set up development environment to develop this theme run: bundle install

To test locally before pushing, start GitBash and run following two commands:
 bundle update
 bundle exec jekyll serve

Then point the browser to indicated Server address: (http://127.0.0.1:4000)

This starts a Jekyll server using content in the test/ directory. As modifications are made to the theme and test site, it will regenerate and you should see the changes in the browser after a refresh.

To upgrade the MM theme refer to: https://mmistakes.github.io/minimal-mistakes/docs/upgrading/

All original tutorial posts with formatting info are included in _drafts folder, which makes them visible only locally when using bundle exec jekyll serve --drafts
