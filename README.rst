Template for the Read the Docs tutorial
=======================================

This GitHub template includes fictional Python library
with some basic Sphinx docs.

Read the tutorial here:

https://docs.readthedocs.io/en/stable/tutorial/



[Read the Docs](https://docs.readthedocs.io/en/stable/index.html)

In this tutorial you will create a documentation project on Read the Docs by importing an Sphinx project from a GitHub repository, tailor its configuration, and explore several useful features of the platform.

The tutorial is aimed at people interested in learning how to use Read the Docs to host their documentation projects. You will fork a fictional software library similar to the one developed in the [official Sphinx tutorial](https://www.sphinx-doc.org/en/master/tutorial/index.html). No prior experience with Sphinx is required, and you can follow this tutorial without having done the Sphinx one.

The only things you will need to follow are a web browser, an Internet connection, and a GitHub account (you can [register for a free account](https://github.com/signup) if you don’t have one). You will use Read the Docs Community, which means that the project will be public.

## Getting started[¶](https://docs.readthedocs.io/en/stable/tutorial/#getting-started "Permalink to this headline")

### Preparing your project on GitHub[¶](https://docs.readthedocs.io/en/stable/tutorial/#preparing-your-project-on-github "Permalink to this headline")

To start, [sign in to GitHub](https://github.com/login) and navigate to [the tutorial GitHub template](https://github.com/readthedocs/tutorial-template/), where you will see a green Use this template button. Click it to open a new page that will ask you for some details:

-   Leave the default “Owner”, or change it to something better for a tutorial project.
    
-   Introduce an appropriate “Repository name”, for example `rtd-tutorial`.
    
-   Make sure the project is “Public”, rather than “Private”.
    

After that, click on the green Create repository from template button, which will generate a new repository on your personal account (or the one of your choosing). This is the repository you will import on Read the Docs, and it contains the following files:

`README.rst`

Basic description of the repository, you will leave it untouched.

`pyproject.toml`

Python project metadata that makes it installable. Useful for automatic documentation generation from sources.

`lumache.py`

Source code of the fictional Python library.

`docs/`

Directory holding all the Sphinx documentation sources, including some required dependencies in `docs/requirements.txt`, the Sphinx configuration `docs/source/conf.py`, and the root document `docs/source/index.rst` written in reStructuredText.

[![GitHub template for the tutorial](https://docs.readthedocs.io/en/stable/_images/github-template.png)](https://docs.readthedocs.io/en/stable/_images/github-template.png)

GitHub template for the tutorial[¶](https://docs.readthedocs.io/en/stable/tutorial/#id3 "Permalink to this image")

### Sign up for Read the Docs[¶](https://docs.readthedocs.io/en/stable/tutorial/#sign-up-for-read-the-docs "Permalink to this headline")

To sign up for a Read the Docs account, navigate to the [Sign Up page](https://readthedocs.org/accounts/signup/) and choose the option Sign up with GitHub. On the authorization page, click the green Authorize readthedocs button.

[![GitHub authorization page](https://docs.readthedocs.io/en/stable/_images/github-authorization.png)](https://docs.readthedocs.io/en/stable/_images/github-authorization.png)

GitHub authorization page[¶](https://docs.readthedocs.io/en/stable/tutorial/#id4 "Permalink to this image")

Note

Read the Docs needs elevated permissions to perform certain operations that ensure that the workflow is as smooth as possible, like installing webhooks. If you want to learn more, check out [Permissions for connected accounts](https://docs.readthedocs.io/en/stable/connected-accounts.html#permissions-for-connected-accounts).

After that, you will be redirected to Read the Docs, where you will need to confirm your e-mail and username. Clicking the Sign Up » button will create your account and redirect you to your [dashboard](https://docs.readthedocs.io/en/stable/glossary.html#term-dashboard).

By now, you should have two email notifications:

-   One from GitHub, telling you that “A third-party OAuth application … was recently authorized to access your account”. You don’t need to do anything about it.
    
-   Another one from Read the Docs, prompting you to “verify your email address”. Click on the link to finalize the process.
    

Finally, you created your account on Read the Docs and are ready to import your first project.

Welcome!

[![Read the Docs empty dashboard](https://docs.readthedocs.io/en/stable/_images/rtd-empty-dashboard.png)](https://docs.readthedocs.io/en/stable/_images/rtd-empty-dashboard.png)

Read the Docs empty dashboard[¶](https://docs.readthedocs.io/en/stable/tutorial/#id5 "Permalink to this image")

Note

Our commercial site offers some extra features, like support for private projects. You can learn more about [our two different sites](https://docs.readthedocs.io/en/stable/choosing-a-site.html).

## First steps[¶](https://docs.readthedocs.io/en/stable/tutorial/#first-steps "Permalink to this headline")

### Importing the project to Read the Docs[¶](https://docs.readthedocs.io/en/stable/tutorial/#importing-the-project-to-read-the-docs "Permalink to this headline")

To import your GitHub project to Read the Docs, first click on the Import a Project button on your dashboard (or browse to [the import page](https://readthedocs.org/dashboard/import/) directly). You should see your GitHub account under the “Filter repositories” list on the right. If the list of repositories is empty, click the 🔄 button, and after that all your repositories will appear on the center.

[![Import projects workflow](https://docs.readthedocs.io/en/stable/_images/rtd-import-projects.gif)](https://docs.readthedocs.io/en/stable/_images/rtd-import-projects.gif)

Import projects workflow[¶](https://docs.readthedocs.io/en/stable/tutorial/#id6 "Permalink to this image")

Locate your `rtd-tutorial` project (possibly clicking next ›› at the bottom if you have several pages of projects), and then click on the ➕ button to the right of the name. The next page will ask you to fill some details about your Read the Docs project:

Name

The name of the project. It has to be unique across all the service, so it is better if you prepend your username, for example `astrojuanlu-rtd-tutorial`.

Repository URL

The URL that contains the sources. Leave the automatically filled value.

Repository type

Version control system used, leave it as “Git”.

Default branch

Name of the default branch of the project, leave it as `main`.

Edit advanced project options

Leave it unchecked, we will make some changes later.

After hitting the Next button, you will be redirected to the [project home](https://docs.readthedocs.io/en/stable/glossary.html#term-project-home). You just created your first project on Read the Docs! 🎉

[![Project home](https://docs.readthedocs.io/en/stable/_images/rtd-project-home.png)](https://docs.readthedocs.io/en/stable/_images/rtd-project-home.png)

Project home[¶](https://docs.readthedocs.io/en/stable/tutorial/#id7 "Permalink to this image")

### Checking the first build[¶](https://docs.readthedocs.io/en/stable/tutorial/#checking-the-first-build "Permalink to this headline")

Read the Docs will try to build the documentation of your project right after you create it. To see the build logs, click on the Your documentation is building link on the [project home](https://docs.readthedocs.io/en/stable/glossary.html#term-project-home), or alternatively navigate to the “Builds” page, then open the one on top (the most recent one).

If the build has not finished yet by the time you open it, you will see a spinner next to a “Installing” or “Building” indicator, meaning that it is still in progress.

[![First successful documentation build](https://docs.readthedocs.io/en/stable/_images/rtd-first-successful-build.png)](https://docs.readthedocs.io/en/stable/_images/rtd-first-successful-build.png)

First successful documentation build[¶](https://docs.readthedocs.io/en/stable/tutorial/#id8 "Permalink to this image")

When the build finishes, you will see a green “Build completed” indicator, the completion date, the elapsed time, and a link to see the corresponding documentation. If you now click on View docs, you will see your documentation live!

[![HTML documentation live on Read the Docs](https://docs.readthedocs.io/en/stable/_images/rtd-first-light.png)](https://docs.readthedocs.io/en/stable/_images/rtd-first-light.png)

HTML documentation live on Read the Docs[¶](https://docs.readthedocs.io/en/stable/tutorial/#id9 "Permalink to this image")

Note

Advertisement is one of our main sources of revenue. If you want to learn more about how do we fund our operations and explore options to go ad-free, check out our [Sustainability page](https://readthedocs.org/sustainability/).

If you don’t see the ad, you might be using an ad blocker. Our Ethical Ads network respects your privacy, doesn’t target you, and tries to be as unobstrusive as possible, so we would like to kindly ask you to [not block us](https://docs.readthedocs.io/en/stable/advertising/ad-blocking.html) ❤️

### Basic configuration changes[¶](https://docs.readthedocs.io/en/stable/tutorial/#basic-configuration-changes "Permalink to this headline")

You can now proceed to make some basic configuration adjustments. Navigate back to the [project page](https://docs.readthedocs.io/en/stable/glossary.html#term-project-page) and click on the ⚙ Admin button, which will open the Settings page.

First of all, add the following text in the description:

> Lumache (/lu’make/) is a Python library for cooks and food lovers that creates recipes mixing random ingredients.

Then set the project homepage to `https://world.openfoodfacts.org/`, and write `food, python` in the list of tags. All this information will be shown on your project home.

After that, configure your email so you get a notification if the build fails. To do so, click on the Notifications link on the left, type the email where you would like to get the notification, and click the Add button. After that, your email will be shown under “Existing Notifications”.

### Trigger a build from a pull request[¶](https://docs.readthedocs.io/en/stable/tutorial/#trigger-a-build-from-a-pull-request "Permalink to this headline")

Read the Docs allows you to [trigger builds from GitHub pull requests](https://docs.readthedocs.io/en/stable/pull-requests.html) and gives you a preview of how the documentation would look like with those changes.

To enable that functionality, first click on the Advanced Settings link on the left under the ⚙ Admin menu, check the “Build pull requests for this project” checkbox, and click the Save button at the bottom of the page.

Next, navigate to your GitHub repository, locate the file `docs/source/index.rst`, and click on the ✏️ icon on the top-right with the tooltip “Edit this file” to open a web editor (more information [on their documentation](https://docs.github.com/en/github/managing-files-in-a-repository/managing-files-on-github/editing-files-in-your-repository)).

[![File view on GitHub before launching the editor](https://docs.readthedocs.io/en/stable/_images/gh-edit.png)](https://docs.readthedocs.io/en/stable/_images/gh-edit.png)

File view on GitHub before launching the editor[¶](https://docs.readthedocs.io/en/stable/tutorial/#id10 "Permalink to this image")

In the editor, add the following sentence to the file:

docs/source/index.rst[¶](https://docs.readthedocs.io/en/stable/tutorial/#id11 "Permalink to this code")

Lumache has its documentation hosted on Read the Docs.

Write an appropriate commit message, and choose the “Create a **new branch** for this commit and start a pull request” option, typing a name for the new branch. When you are done, click the green Propose changes button, which will take you to the new pull request page, and there click the Create pull request button below the description.

[![Read the Docs building the pull request from GitHub](https://docs.readthedocs.io/en/stable/_images/gh-pr-build.png)](https://docs.readthedocs.io/en/stable/_images/gh-pr-build.png)

Read the Docs building the pull request from GitHub[¶](https://docs.readthedocs.io/en/stable/tutorial/#id12 "Permalink to this image")

After opening the pull request, a Read the Docs check will appear indicating that it is building the documentation for that pull request. If you click on the Details link while it is building, you will access the build logs, otherwise it will take you directly to the documentation. When you are satisfied, you can merge the pull request!

## Customizing the build process[¶](https://docs.readthedocs.io/en/stable/tutorial/#customizing-the-build-process "Permalink to this headline")

The Settings page of the [project home](https://docs.readthedocs.io/en/stable/glossary.html#term-project-home) allows you to change some _global_ configuration values of your project. In addition, you can further customize the building process using the `.readthedocs.yaml` [configuration file](https://docs.readthedocs.io/en/stable/config-file/v2.html). This has several advantages:

-   The configuration lives next to your code and documentation, tracked by version control.
    
-   It can be different for every version (more on versioning in the next section).
    
-   Some configurations are only available using the config file.
    

Read the Docs works without this configuration by [making some decisions on your behalf](https://docs.readthedocs.io/en/stable/builds.html#default-versions-of-dependencies). For example, what Python version to use, how to install the requirements, and others.

Tip

Settings that apply to the entire project are controlled in the web dashboard, while settings that are version or build specific are better in the YAML file.

### Upgrading the Python version[¶](https://docs.readthedocs.io/en/stable/tutorial/#upgrading-the-python-version "Permalink to this headline")

For example, to explicitly use Python 3.8 to build your project, navigate to your GitHub repository, click on the Add file button, and add a `.readthedocs.yaml` file with these contents to the root of your project:

.readthedocs.yaml[¶](https://docs.readthedocs.io/en/stable/tutorial/#id13 "Permalink to this code")

version: 2

build:
  os: "ubuntu-20.04"
  tools:
    python: "3.8"

The purpose of each key is:

`version`

Mandatory, specifies [version 2 of the configuration file](https://docs.readthedocs.io/en/stable/config-file/v2.html).

`build.os`

Required to specify the Python version, [states the name of the base image](https://docs.readthedocs.io/en/stable/config-file/v2.html#build-os).

`build.tools.python`

Declares the Python version to be used.

After you commit these changes, go back to your project home, navigate to the “Builds” page, and open the new build that just started. You will notice that one of the lines contains `python3.8`: if you click on it, you will see the full output of the corresponding command, stating that it used Python 3.8.6 to create the virtual environment.

[![Read the Docs build using Python 3.8](https://docs.readthedocs.io/en/stable/_images/build-python3.8.png)](https://docs.readthedocs.io/en/stable/_images/build-python3.8.png)

Read the Docs build using Python 3.8[¶](https://docs.readthedocs.io/en/stable/tutorial/#id14 "Permalink to this image")

### Making warnings more visible[¶](https://docs.readthedocs.io/en/stable/tutorial/#making-warnings-more-visible "Permalink to this headline")

If you navigate to your HTML documentation, you will notice that the index page looks correct, but actually the API section is empty. This is a very common issue with Sphinx, and the reason is stated in the build logs. On the build page you opened before, click on the View raw link on the top right, which opens the build logs in plain text, and you will see several warnings:

WARNING: \[autosummary\] failed to import 'lumache': no module named lumache
...
WARNING: autodoc: failed to import function 'get\_random\_ingredients' from module 'lumache'; the following exception was raised:
No module named 'lumache'
WARNING: autodoc: failed to import exception 'InvalidKindError' from module 'lumache'; the following exception was raised:
No module named 'lumache'

To spot these warnings more easily and allow you to address them, you can add the `sphinx.fail_on_warning` option to your Read the Docs configuration file. For that, navigate to GitHub, locate the `.readthedocs.yaml` file you created earlier, click on the ✏️ icon, and add these contents:

.readthedocs.yaml[¶](https://docs.readthedocs.io/en/stable/tutorial/#id15 "Permalink to this code")

version: 2

build:
  os: "ubuntu-20.04"
  tools:
    python: "3.8"

sphinx:
 fail\_on\_warning: true 

At this point, if you navigate back to your “Builds” page, you will see a `Failed` build, which is exactly the intended result: the Sphinx project is not properly configured yet, and instead of rendering an empty API page, now the build fails.

The reason [`sphinx.ext.autosummary`](https://www.sphinx-doc.org/en/master/usage/extensions/autosummary.html#module-sphinx.ext.autosummary "(in Sphinx v5.0.0+)") and [`sphinx.ext.autodoc`](https://www.sphinx-doc.org/en/master/usage/extensions/autodoc.html#module-sphinx.ext.autodoc "(in Sphinx v5.0.0+)") fail to import the code is because it is not installed. Luckily, the `.readthedocs.yaml` also allows you to specify which requirements to install.

To install the library code of your project, go back to editing `.readthedocs.yaml` on GitHub and modify it as follows:

.readthedocs.yaml[¶](https://docs.readthedocs.io/en/stable/tutorial/#id16 "Permalink to this code")

python:
 \# Install our python package before building the docs install: \- method: pip      path: .

With this change, Read the Docs will install the Python code before starting the Sphinx build, which will finish seamlessly. If you go now to the API page of your HTML documentation, you will see the `lumache` summary!

### Enabling PDF and EPUB builds[¶](https://docs.readthedocs.io/en/stable/tutorial/#enabling-pdf-and-epub-builds "Permalink to this headline")

Sphinx can build several other formats in addition to HTML, such as PDF and EPUB. You might want to enable these formats for your project so your users can read the documentation offline.

To do so, add this extra content to your `.readthedocs.yaml`:

.readthedocs.yaml[¶](https://docs.readthedocs.io/en/stable/tutorial/#id17 "Permalink to this code")

sphinx:
  fail\_on\_warning: true

formats:
 \- pdf \- epub 

After this change, PDF and EPUB downloads will be available both from the “Downloads” section of the [project home](https://docs.readthedocs.io/en/stable/glossary.html#term-project-home), as well as the [flyout menu](https://docs.readthedocs.io/en/stable/glossary.html#term-flyout-menu).

![Downloads available from the flyout menu](https://docs.readthedocs.io/en/stable/_images/flyout-downloads.png)

Downloads available from the flyout menu[¶](https://docs.readthedocs.io/en/stable/tutorial/#id18 "Permalink to this image")

## Versioning documentation[¶](https://docs.readthedocs.io/en/stable/tutorial/#versioning-documentation "Permalink to this headline")

Read the Docs allows you to have [several versions of your documentation](https://docs.readthedocs.io/en/stable/versions.html), in the same way that you have several versions of your code. By default, it creates a `latest` version that points to the default branch of your version control system (`main` in the case of this tutorial), and that’s why the URLs of your HTML documentation contain the string `/latest/`.

### Creating a new version[¶](https://docs.readthedocs.io/en/stable/tutorial/#creating-a-new-version "Permalink to this headline")

Let’s say you want to create a `1.0` version of your code, with a corresponding `1.0` version of the documentation. For that, first navigate to your GitHub repository, click on the branch selector, type `1.0.x`, and click on “Create branch: 1.0.x from ‘main’” (more information [on their documentation](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository)).

Next, go to your [project home](https://docs.readthedocs.io/en/stable/glossary.html#term-project-home), click on the Versions button, and under “Active Versions” you will see two entries:

-   The `latest` version, pointing to the `main` branch.
    
-   A new `stable` version, pointing to the `origin/1.0.x` branch.
    

[![List of active versions of the project](https://docs.readthedocs.io/en/stable/_images/active-versions.png)](https://docs.readthedocs.io/en/stable/_images/active-versions.png)

List of active versions of the project[¶](https://docs.readthedocs.io/en/stable/tutorial/#id19 "Permalink to this image")

Right after you created your branch, Read the Docs created a new special version called `stable` pointing to it, and started building it. When the build finishes, the `stable` version will be listed in the [flyout menu](https://docs.readthedocs.io/en/stable/glossary.html#term-flyout-menu) and your readers will be able to choose it.

Note

Read the Docs [follows some rules](https://docs.readthedocs.io/en/stable/versions.html#how-we-envision-versions-working) to decide whether to create a `stable` version pointing to your new branch or tag. To simplify, it will check if the name resembles a version number like `1.0`, `2.0.3` or `4.x`.

Now you might want to set `stable` as the _default version_, rather than `latest`, so that users see the `stable` documentation when they visit the [root URL](https://docs.readthedocs.io/en/stable/glossary.html#term-root-URL) of your documentation (while still being able to change the version in the flyout menu).

For that, go to the Advanced Settings link under the ⚙ Admin menu of your project home, choose `stable` in the “Default version\*” dropdown, and hit Save at the bottom. Done!

### Modifying versions[¶](https://docs.readthedocs.io/en/stable/tutorial/#modifying-versions "Permalink to this headline")

Both `latest` and `stable` are now _active_, which means that they are visible for users, and new builds can be triggered for them. In addition to these, Read the Docs also created an _inactive_ `1.0.x` version, which will always point to the `1.0.x` branch of your repository.

[![List of inactive versions of the project](https://docs.readthedocs.io/en/stable/_images/inactive-versions.png)](https://docs.readthedocs.io/en/stable/_images/inactive-versions.png)

List of inactive versions of the project[¶](https://docs.readthedocs.io/en/stable/tutorial/#id20 "Permalink to this image")

Let’s activate the `1.0.x` version. For that, go to the “Versions” on your [project home](https://docs.readthedocs.io/en/stable/glossary.html#term-project-home), locate `1.0.x` under “Activate a version”, and click on the Activate button. This will take you to a new page with two checkboxes, “Active” and “Hidden”. Check only “Active”, and click Save.

After you do this, `1.0.x` will appear on the “Active Versions” section, and a new build will be triggered for it.

### Show a warning for old versions[¶](https://docs.readthedocs.io/en/stable/tutorial/#show-a-warning-for-old-versions "Permalink to this headline")

When your project matures, the number of versions might increase. Sometimes you will want to warn your readers when they are browsing an old or outdated version of your documentation.

To showcase how to do that, let’s create a `2.0` version of the code: navigate to your GitHub repository, click on the branch selector, type `2.0.x`, and click on “Create branch: 2.0.x from ‘main’”. This will trigger two things:

-   Since `2.0.x` is your newest branch, `stable` will switch to tracking it.
    
-   A new `2.0.x` version will be created on your Read the Docs project.
    
-   Since you already have an active `stable` version, `2.0.x` will be activated.
    

From this point, `1.0.x` version is no longer the most up to date one. To display a warning to your readers, go to the ⚙ Admin menu of your project home, click on the Advanced Settings link on the left, enable the “Show version warning” checkbox, and click the Save button.

If you now browse the `1.0.x` documentation, you will see a warning on top encouraging you to browse the latest version instead. Neat!

[![Warning for old versions](https://docs.readthedocs.io/en/stable/_images/old-version-warning.png)](https://docs.readthedocs.io/en/stable/_images/old-version-warning.png)

Warning for old versions[¶](https://docs.readthedocs.io/en/stable/tutorial/#id21 "Permalink to this image")

## Getting insights from your projects[¶](https://docs.readthedocs.io/en/stable/tutorial/#getting-insights-from-your-projects "Permalink to this headline")

Once your project is up and running, you will probably want to understand how readers are using your documentation, addressing some common questions like:

-   what pages are the most visited pages?
    
-   what search terms are the most frequently used?
    
-   are readers finding what they look for?
    

Read the Docs offers you some analytics tools to find out the answers.

### Browsing Traffic Analytics[¶](https://docs.readthedocs.io/en/stable/tutorial/#browsing-traffic-analytics "Permalink to this headline")

The [Traffic Analytics](https://docs.readthedocs.io/en/stable/analytics.html) view shows the top viewed documentation pages of the past 30 days, plus a visualization of the daily views during that period. To generate some artificial views on your newly created project, you can first click around the different pages of your project, which will be accounted immediately for the current day statistics.

To see the Traffic Analytics view, go back the [project page](https://docs.readthedocs.io/en/stable/glossary.html#term-project-page) again, click on the ⚙ Admin button, and then click on the Traffic Analytics section. You will see the list of pages in descending order of visits, as well as a plot similar to the one below.

[![Traffic Analytics plot](https://docs.readthedocs.io/en/stable/_images/traffic-analytics-plot.png)](https://docs.readthedocs.io/en/stable/_images/traffic-analytics-plot.png)

Traffic Analytics plot[¶](https://docs.readthedocs.io/en/stable/tutorial/#id22 "Permalink to this image")

Note

The Traffic Analytics view explained above gives you a simple overview of how your readers browse your documentation. It has the advantage that it stores no identifying information about your visitors, and therefore it respects their privacy. However, you might want to get more detailed data by [enabling Google Analytics](https://docs.readthedocs.io/en/stable/analytics.html#enabling-google-analytics-on-your-project). Notice though that we take some extra measures to [respect user privacy](https://docs.readthedocs.io/en/stable/advertising/advertising-details.html#analytics) when they visit projects that have Google Analytics enabled, and this might reduce the number of visits counted.

Finally, you can also download this data for closer inspection. To do that, scroll to the bottom of the page and click on the Download all data button. That will prompt you to download a CSV file that you can process any way you want.

### Browsing Search Analytics[¶](https://docs.readthedocs.io/en/stable/tutorial/#browsing-search-analytics "Permalink to this headline")

Apart from traffic analytics, Read the Docs also offers the possibility to inspect [what search terms your readers use](https://docs.readthedocs.io/en/stable/server-side-search.html#search-analytics) on your documentation. This can inform decisions on what areas to reinforce, or what parts of your project are less understood or more difficult to find.

To generate some artificial search statistics on the project, go to the HTML documentation, locate the Sphinx search box on the left, type `ingredients`, and press the Enter key. You will be redirected to the search results page, which will show two entries.

Next, go back to the ⚙ Admin section of your project page, and then click on the Search Analytics section. You will see a table with the most searched queries (including the `ingredients` one you just typed), how many results did each query return, and how many times it was searched. Below the queries table, you will also see a visualization of the daily number of search queries during the past 30 days.

[![Most searched terms](https://docs.readthedocs.io/en/stable/_images/search-analytics-terms.png)](https://docs.readthedocs.io/en/stable/_images/search-analytics-terms.png)

Most searched terms[¶](https://docs.readthedocs.io/en/stable/tutorial/#id23 "Permalink to this image")

Like the Traffic Analytics, you can also download the whole dataset in CSV format by clicking on the Download all data button.

## Where to go from here[¶](https://docs.readthedocs.io/en/stable/tutorial/#where-to-go-from-here "Permalink to this headline")

This is the end of the tutorial. You started by forking a GitHub repository and importing it on Read the Docs, building its HTML documentation, and then went through a series of steps to customize the build process, tweak the project configuration, and add new versions.

Here you have some resources to continue learning about documentation and Read the Docs:

-   You can learn more about the functionality of the platform by going over our [Read the Docs features](https://docs.readthedocs.io/en/stable/features.html) page.
    
-   To make the most of the documentation generators that are supported, you can read the [Sphinx tutorial](https://www.sphinx-doc.org/en/master/tutorial/index.html) or the [MkDocs User Guide](https://www.mkdocs.org/user-guide/).
    
-   Whether you are a documentation author, a project administrator, a developer, or a designer, you can follow our how-to guides that cover specific tasks, available under [Guides](https://docs.readthedocs.io/en/stable/guides/index.html).
    
-   You can check out some of the [Advanced features of Read the Docs](https://docs.readthedocs.io/en/stable/index.html#advanced-features-of-read-the-docs), like [Subprojects](https://docs.readthedocs.io/en/stable/subprojects.html) or [Automation Rules](https://docs.readthedocs.io/en/stable/automation-rules.html), to name a few.
    
-   For private project support and other enterprise features, you can use [our commercial service](https://docs.readthedocs.io/en/stable/commercial/index.html) (and if in doubt, check out [Choosing Between Our Two Sites](https://docs.readthedocs.io/en/stable/choosing-a-site.html)).
    
-   Do you want to join a global community of fellow `documentarians`? Check out [Write the Docs](https://www.writethedocs.org/) and [its Slack workspace](https://www.writethedocs.org/slack/ "(in Write the Docs v1.0)").
    
-   Do you want to [contribute to Read the Docs](https://docs.readthedocs.io/en/stable/contribute.html)? We greatly appreciate it! Check out [Building and Contributing to Documentation](https://docs.readthedocs.io/en/stable/development/docs.html).
    

Happy documenting!
