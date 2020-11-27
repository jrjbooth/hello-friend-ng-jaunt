# Hello Friend NG Jaunt

A variant of the Hello Friend NG theme with some Jaunty accents and angles.

## How to configure

The theme doesn't require any advanced configuration. Just copy the following config file.
To see all possible configurations, [check the docs](docs/config.md).
Note: There are more options to configure. Take a look into the `config.toml` in `exampleSite`.

``` toml
baseurl      = "localhost"
title        = "My Blog"
languageCode = "en-us"
theme        = "hello-friend-ng-jaunt"
paginate     = 10

[params]
  dateform        = "Jan 2, 2006"
  dateformShort   = "Jan 2"
  dateformNum     = "2006-01-02"
  dateformNumTime = "2006-01-02 15:04"

  # Subtitle for home
  homeSubtitle = "A simple and beautiful blog"

  # Set disableReadOtherPosts to true in order to hide the links to other posts.
  disableReadOtherPosts = false

  # Enable sharing buttons, if you like
  enableSharingButtons = true

  # Metadata mostly used in document's head
  description = "My new homepage or blog"
  keywords = "homepage, blog"
  images = [""]

  # Default theme "light" or "dark"
  defaultTheme = "dark"

[taxonomies]
    category = "blog"
    tag      = "tags"
    series   = "series"

[languages]
  [languages.en]
    title = "Hello Friend NG"
    subtitle = "A simple theme for Hugo"
    keywords = ""
    copyright = '<a href="https://creativecommons.org/licenses/by-nc/4.0/" target="_blank" rel="noopener">CC BY-NC 4.0</a>'
    readOtherPosts = "Read other posts"

    [languages.en.params.logo]
      logoText = "hello friend ng"
      logoHomeLink = "/"
    # or
    #
    # path = "/img/your-example-logo.svg"
    # alt = "Your example logo alt text"

  # And you can even create generic menu
  [[menu.main]]
    identifier = "blog"
    name       = "Blog"
    url        = "/posts"
```

## More things

### Built-in shortcodes

Of course you are able to use all default shortcodes from hugo (https://gohugo.io/content-management/shortcodes/).

#### image

Properties:

  - `src` (required)
  - `alt` (optional)
  - `position` (optional, default: `left`, options: [`left`, `center`, `right`])
  - `style`

Example:

``` golang
{{< image src="/img/hello.png" alt="Hello Friend" position="center" style="border-radius: 8px;" >}}
```

### Code highlighting

Supported languages: [Take a look here](https://prismjs.com/download.html#themes=prism-tomorrow&languages=markup+css+clike+javascript+abap+actionscript+ada+apacheconf+apl+applescript+c+arff+asciidoc+asm6502+csharp+autohotkey+autoit+bash+basic+batch+bison+brainfuck+bro+cpp+aspnet+arduino+cil+coffeescript+clojure+ruby+csp+css-extras+d+dart+diff+markup-templating+docker+eiffel+elixir+elm+lua+erb+erlang+fsharp+flow+fortran+gcode+gedcom+gherkin+git+glsl+gml+go+graphql+groovy+less+handlebars+haskell+haxe+hcl+http+hpkp+hsts+ichigojam+icon+inform7+ini+io+j+java+scala+php+javastacktrace+jolie+n4js+markdown+json+julia+keyman+kotlin+latex+crystal+scheme+liquid+lisp+livescript+lolcode+makefile+django+matlab+mel+mizar+monkey+n1ql+typescript+nand2tetris-hdl+nasm+nginx+nim+nix+nsis+objectivec+ocaml+opencl+oz+parigp+parser+pascal+perl+php-extras+sql+powershell+processing+prolog+properties+protobuf+scss+puppet+pure+python+q+qore+r+jsx+renpy+reason+vala+rest+rip+roboconf+textile+rust+plsql+sass+stylus+smalltalk+smarty+soy+sas+twig+swift+yaml+tcl+haml+toml+tt2+pug+tsx+visual-basic+vbnet+velocity+verilog+vhdl+vim+wasm+wiki+xeora+xojo+xquery+tap)

By default the theme is using PrismJS to color your code syntax. All you need to do is to wrap you code like this:

<pre>
``` html
  // your code here
```
</pre>

### Favicon

Check the [docs](docs/favicons.md).

## Social Icons:

Take a look into this [list](docs/svgs.md)

If you need another one, just open an issue or create a pull request with your wished icon. :)

## Known issues

There is a bug in Hugo that sometimes causes the main page not to render correctly. The reason is an empty taxonomy part.
Related issue tickets: [!14](https://github.com/rhazdon/hugo-theme-hello-friend-ng/issues/14) [!59](https://github.com/rhazdon/hugo-theme-hello-friend-ng/issues/59).

Either you comment it out completely or you write the following in

``` toml
[taxonomies]
  tag      = "tags"
  category = "categories"
```

## How to edit the theme

Just edit it. You don't need any node stuff.

## Licence

The theme is released under the [MIT License](https://github.com/jrjbooth/hello-friend-ng-jaunt/blob/master/LICENSE.md).
