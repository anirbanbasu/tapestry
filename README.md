# Tapestry

Tapestry is a researcher profile website theme for the [Zola static site generator](https://www.getzola.org/).

Inspired by and derived from the [terminus theme](https://github.com/ebkalderon/terminus), specifically its `aa8d8b67f9ab69ae48e1405f96e152d41f03e0ed` commit, tapestry inherits a number of features from the terminus theme. The key differences include the following.

- A number of presentation styles (e.g., `creative`), each with a number of variants (e.g., `editorial-zine`) replace the `extra.color_scheme` setting of the terminus theme.
- Each presentation style and its variants are available in both light and dark modes.
- Additional shortcodes, such as for showing the colour palette.

Try the demo at the following links.

- [https://ghp-tapestry.netlify.app](https://ghp-tapestry.netlify.app)
- [https://ghp-tapestry.anirbanbasu.com](https://ghp-tapestry.anirbanbasu.com)

![Tapestry screenshot](screenshot.png)

## Usage

1. Initialise a Git repository in your [Zola project directory](https://www.getzola.org/documentation/getting-started/cli-usage/#init), if you have not done it.

   ```bash
   git init
   ```

2. Add this theme as a Git submodule.

   ```bash
   git submodule add https://github.com/anirbanbasu/tapestry.git themes/tapestry
   ```

3. Enable this theme in your `config.toml`:

   ```toml
   theme = "tapestry"
   ```

4. Set a website `title` of your liking in your  `config.toml`:

   ```toml
   title = "My research profile"
   ```

5. Create a text file named `content/_index.md`. This file controls how your home page looks. Choose _exactly one_ of the following options:

   1. **Serve yours posts from `/`:**

      ```markdown
      +++
      title = "Home"
      paginate_by = 5  # Show 5 posts per page.
      +++
      ```

   2. **Serve posts from a different path, e.g. `posts/`:**

      ```markdown
      +++
      title = "Home"

      [extra]
      section_path = "posts/_index.md"  # Where to find your posts.
      max_posts = 5  # Show 5 posts and a link to posts section on home page.
      +++
      ```


## License

This project is licensed under the terms of the [MIT license](LICENSE).
