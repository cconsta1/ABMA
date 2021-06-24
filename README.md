# ABMA Website 
These are website maintenance instructions for the Agent-Based Modeling for Archaeology website.

## An overview
The website theme code is accessed through `ABMA/config.yml`. Here we have used the Jekyll theme "Minimal", which is called in `theme: jekyll-theme-minimal`. The title of the of the website (that appears in the main section, not the left sidebar) is called in `title: Agent-Based Modeling for Archaeology`. We use `logo:` to create the picture in the sidebar. We use `show_downloads: false` so that any GitHub, ZIP File, or TAR Ball downloads that might show up do not actually show up (we needed to save space to have all of the chapter headings in the sidebar). 

## How to change the website
To make changes to the website, navigate through `SantaFeInstitute` --> `ABMA` and select `gh-pages` from the **master** dropdown above the individual chapter folders. (If you are here, you have already done that. Congratulations!)

## General changes to the static sidebar
To make changes to the static sidebar on the left-hand side of the website, stay in the `ABMA` section, go to the layouts folder `_layouts`, and select the `default.html` document. In order to make and save changes to the sidebar, you will need to click on `default.html` and then the pencil icon in the upper right-hand corner of the light gray bar above the html text. Any changes that you make will need to be saved by clicking on the green "Commit changes" button at the bottom of the page (leave the button next to "Commit directly to the `gh-pages` branch." selected). 

## Changing text color, background color, and text
The following code changes the text and color of the header at the top of the left sidebar. The html color hexcode `"#000000"` makes the text black. To add a background color behind the text, add in `style="background-color: #000000"` (in this instance the zeros will make the background color black. The complete code with a background color added would look like this:` <p style="background-color: #000000" style="color: #000000">`. Change the text by changing the text of "Agent-Based Modeling for Archaeology" in the following section: `<Agent-Based Modeling for Archaeology</p>`. \
        `<h1>` \
          `<p style="color: #000000">Agent-Based Modeling for Archaeology</p>` \
        `</h1>` 

## Anchors
The anchors on the sidebar are put in place with the following code:

(1)      `<a style="color: #E66100" href="#INTRODUCTION">Ch. 0 • Introduction</a>` \
(2)      `<a href="path/to/contributing/index.md#INTRODUCTION">`
      
The text `>Ch. 0 • Introduction</a>` will appear in the sidebar as a clickable link. The `href="path/to/contributing/index.md#INTRODUCTION">` is the code that makes the anchor work. This references the following code in the `index.md`:
  
(3)      `<a name="INTRODUCTION"></a>` \
(4)      `### INTRODUCTION: The Art & Science of Building Societies in Silico`

which, along with the href part of (1), relies on the `name="INTRODUCTION">` being *above* the actual Introduction title in order for the anchor to redirect to the title. If `name="INTRODUCTION">` were located underneath the actual Introduction title, the anchor redirection would omit the title and direct the readers straight to the chapter description. 
  
