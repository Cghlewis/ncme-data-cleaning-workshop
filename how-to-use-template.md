## How to use this workshop template

1.  Create your new repository from this template repository by following this
    [GitHub Docs
    page](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template).

2.  Edit `README.md` to remove the template instructions and include your
    specific workshop details.

3.  Preview the website by running `quarto preview` in the `Terminal`. As you
    edit in the following steps, the preview will update in your browser at
    `http://localhost:3434/`.

4.  Edit `_quarto.yml` to include your workshop name, logos, and URLs.

5.  Edit website content in root directory:

    -   `index.qmd` is the home page.

    -   `prework.qmd` lists tasks for attendees to complete before the workshop.

    -   `materials.qmd` includes a link to the full screen slides, an iframe
        with the slides, video recording of the workshop, and exercises.

6.  Edit website styling.

    -   To remove custom styling and choose a basic [bootswatch
        theme](https://quarto.org/docs/output-formats/html-themes.html#overview),
        in `_quarto.yml`, change `theme: [flatly, theme.scss]` to
        `theme: flatly`, or the theme of your choosing.

    -   To customize the colors and fonts of my custom styling, open
        `theme.scss` and change the values for the `$theme-` variables.

        -   If using a different Google Font, change the `@import` [web embed
            code](https://fonts.google.com/selection/embed) include the fonts
            you want.

        -   Replace the `primary`, `secondary`, and `light` colors with hex
            codes you want.

    -   [Quarto Docs on HTML
        theming](https://quarto.org/docs/output-formats/html-themes.html#basic-options)

7.  Edit slides content and styling within the `slides` subfolder.

    -   Edit content in `index.qmd`. I left my intro slides to demonstrate
        different Reveal JS and Quarto features including:

        -   Images using a special class to center
            (`![](images/rladies-abuja.png){.center fig-alt="R-Ladies Abuja Logo"}`)

        -   [FontAwesome icons](https://github.com/quarto-ext/fontawesome)
            followed by a link
            `{{< fa link size=xl >}} [jadeyryan.com](https://jadeyryan.com)`

        -   [Columns](https://quarto.org/docs/presentations/revealjs/#multiple-columns)

        -   [Code line number
            highlighting](https://quarto.org/docs/presentations/revealjs/#line-highlighting)
            example shows all lines at first, then just the first, and then the
            third and fourth together

        -   [Incremental
            lists](https://quarto.org/docs/presentations/revealjs/#incremental-lists)
            for number and bullet lists

        -   [Pauses](https://quarto.org/docs/presentations/revealjs/#incremental-lists)
            increment content that is not a list

        -   Section break slides (use `{.background-primary}` or
            `{.background-secondary}` with a level 1 heading (`#`)

        -   Custom footer for a specific slide
        
        -   [`{countdown}`](https://github.com/gadenbuie/countdown) timer for exercises

    -   Edit styling.

        -   To remove custom styling and choose a basic [Reveal
            theme](https://quarto.org/docs/presentations/revealjs/#themes), in
            the YAML heading of `slides/index.qmd`, change `theme: slides.scss`
            to `theme: solarized`, or the theme of your choosing.

        -   To customize the colors and fonts of my custom styling, open
            `theme.scss` and change the values for the `$theme-` variables. If
            using a different Google Font, change the `@import` [web embed
            code](https://fonts.google.com/selection/embed) include the fonts
            you want.

8.  When ready to publish, run `quarto render` in the `Terminal`. Commit and
    push your changes to the repo, which will trigger a deployment of your site.

    -   For the first time you publish, you will need to configure your GitHub
        repository to publish from the `docs` directory of your `main` branch.

    -   Alternatively, run `quarto publish gh-pages` in the `Terminal` if your
        repository is configured according to these
        [instructions](https://quarto.org/docs/publishing/github-pages.html#publish-command).
