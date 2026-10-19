Beyond Pass or Fail
What the Bechdel Test Can Teach Us About Bayesian Inference

A Quarto website for students who have finished a probability course (such as STAT 360) and know frequentist methods. It introduces Bayesian inference through one question: what proportion of movies pass the Bechdel test?

The site walks from that question through a brief frequentist analysis, then through priors, Bayes' rule, the posterior mean, shrinkage, sequential updating, and a comparison of the two approaches.

Author: Nabiha Tahsin

Hosting
-------
The live site is on GitHub Pages:

    https://nabiiinabi.github.io/tailored-proj/

Pages is set to the legacy source: the docs/ folder on the main branch of https://github.com/nabiiinabi/tailored-proj. Pushing a rendered docs/ folder to main publishes the site. There is no GitHub Actions workflow. HTTPS is enforced.

Quarto writes the site into docs/. A .nojekyll file is copied there so GitHub Pages does not run Jekyll, which would hide folders whose names start with an underscore.

How the site is organized
-------------------------
index.qmd              Home
the-question.qmd       The Question
section-1-2.qmd        From Twenty Movies to an Unknown Proportion
section-3-4.qmd        Two Ways to Describe Uncertainty
section-5.qmd          A Brief Frequentist Analysis
section-6-7.qmd        Beginning the Bayesian Analysis
section-8-9.qmd        What Do Alpha and Beta Control?
section-10-11.qmd      Updating with Bayes' Rule
section-12-13.qmd      The Posterior Mean and Shrinkage
section-14-15.qmd      Does the Prior Change the Conclusion?
section-16-17.qmd      Learning One Movie at a Time
section-18.qmd         Tweets After a Movie Release
section-19-20.qmd      Comparing the Frequentist and Bayesian Results
section-21.qmd         Conclusions and Takeaways

Sidebar order and page labels live in _quarto.yml. Page titles come from each .qmd file. Colors and layout overrides are in theme-light.scss, on top of Quarto's journal theme. Figures are built with Observable JS (ojs) chunks; the code that builds them is hidden in the rendered site.

Build
-----
Requires Quarto (https://quarto.org).

Preview locally:

    quarto preview

Render the site into docs/:

    quarto render

docs/ is the website output that GitHub Pages serves. Commit and push it to main to update the live site.
