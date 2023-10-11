# Journalist's Guide to Analyzing Data in R

## Credit

This template is based off a checklist that was created from a
combination of personal experience from the Hearst Data Teams and NICAR
presentations from MaryJo Webster, Christian McDonald, Shawn McIntosh,
Rebecca Lindstrom, Aaron Kessler and Alexander Cohen.

Methodology checks were added by Libby Seline.

## Checklist

### Pre-analysis steps

-   [ ] Research what our newsrooms have done on the topic you're about
    to find data for. If you already have a data source you want to use,
    look to see if we've used something else in the past. Why are we
    switching things up now?
-   [ ] Research sources for your data. Once you find a good source,
    research who has used it before. Other journalism article, agency
    reports, academic articles.
-   [ ] Understand why and how the data are collected. This will help
    you understand the context of the data and any caveats it might
    contain.
    -   Methodology checks:

        -   [ ] You have data in a ready to use file OR have a plan to
            extract the data from a PDF

        -   [ ] The source is an organization dedicated to researching
            this issue and other adjacent topics

        -   [ ] Has a published methodology that includes information
            about when, where, why, how the data was collected

        -   [ ] Is ideally not relying on a data from an alternate
            source (aka a government organization)

            -    Your data team may want to conduct their own analysis
                OR it may contradict existing analysis

        -   [ ] Did NOT include survey data

            -   It has potential to be risky because survey data can be
                affected by many outside factors

        -   [ ] Does include a large sample size and has a small margin
            of error

        -   [ ] The data is NOT just a population map

        -   [ ] Includes rates rather than number of [incidents]

        -   [ ] You know precisely what the data is measuring You know
            what factors may have affected data collection

            -   Ex: Car accidents during the pandemic → was there an
                increase in accidents post-pandemic? Yes! But that's due
                to the pandemic
-   [ ] Talk to humans (agency nerds) about the data. Usually this will
    be the people who created it, but it might also be people who use
    the data regularly (academics).
-   [ ] Make sure you understand EVERY COLUMN. Just because you're not
    using the column doesn't mean you don't need to understand what it
    means.
-   [ ] Develop your hypothesis. What do you want to prove/disprove with
    your data analysis?
-   [ ] Write questions you want the data to answer

### Organizational steps

Without organization, your projects will be prone to errors.
Additionally, your future self and other coworkers will thank you for
it.

-   [ ] Save a clean copy of your data that you won't ever touch. NOT IN
    YOUR EMAIL. Save it on the drive and/or on your computer.

-   [ ] Use folder and filename naming conventions. Nest
    project-specific files in a project folder. Include dates, source
    indication and minimal description in filenames. Never name things
    like: final-analysis.csv

-   [ ] Keep a data diary of what you do to the data. This can be a
    google doc, a Jupyter notebook or RStudio script comments.

### Analysis and pitching steps

-   [ ] Many of these steps are asking you to not just wait for problems
    in the data to present themselves, but to actively LOOK for problems
    before you start answering your data questions.

-   [ ] Figure out which columns have null values (some aggregators
    won't count records with null values in the agg field. This can be
    an issue if you think it's returning everything.)

-   [ ] Figure out max/min for each column

-   [ ] Make sure data types for each column match what you think they
    should be. Sometimes numbers can be saved as strings because there
    are non-numeric values hidden among all the numbers. This can be an
    issue.

-   [ ] For string columns, make sure there aren't any
    spelling/capitalization issues that will skew your results.

-   [ ] Identify outliers for used columns and make sure they're not
    crap data/mistakes. If you find an insane outlier that you want to
    use for your "star" finding, ask yourself if this is too good to be
    true.

-   [ ] Look for duplicate rows

-   [ ] Make sure you understand the universe of your data. Maybe you
    assume the universe is "unique humans" but actually it's "arrest
    incidents" and a single human might be represented multiple times.

-   [ ] Make a distinction between "analysis graphics" and "publishable
    graphics".

    -   Analysis graphics are to help you and your reporting mates
        understand the data. Most of these will likely NOT be published.

    -   Published graphics are developed to work with the story and
        contain only necessary information.

-   [ ] Pull out your "star" finding and use that to create your story
    pitch. Make sure to include any possible issues with the data and if
    you're going to need more data or further interviews to create the
    final product (article).

-   [ ] Try to present the data in context of other reporting you or the
    newsroom has done on the subject.

### Post-analysis/fact-checking steps

-   Be wary of sharing your "findings" with people (other than your
    friendly data editor and data team peers) until you're sure about
    your results or need some additional context to understand them
    further. When people hear that you have "findings" it can make them
    over excited and wanna rush.

-   [ ] Hand calculate some of your results as a spot-checking method

-   [ ] Double check your custom functions and equations (or ask someone
    else to check them!) Are they correct?

-   [ ] Rerun your analysis. Do you get the same results?

-   [ ] If possible, verify your findings IRL. Do they make sense? What
    could be accounting for your unexpected findings?

-   [ ] Walk your editor through your process/code.

-   [ ] If possible, go back to the agency/org that you got the data
    from and confirm your findings. This is sometimes not possible.

### Writing steps

-   Make numbers relatable. Bring them down to a unit that our readers
    will understand. If a company uses 5 million gallons of water, what
    is that relative to what a normal household uses?

-   Don't make readers do math. Don't say: 10 people live in this
    neighborhood and 7 are black. Say 70% of the neighborhood is black.

-   Reduce the number of decimals you use.

-   Consider what is a good number and what is a bad number. If a city
    has a poverty rate of 12%, is that good or bad? You may need to turn
    to academics or other researchers for this info.

-   Instead of using lots of numbers, tell the reader what the trend is.
    Let your charts, graphs and maps handle the detail data work.

-   Don't be afraid to paraphrase non-essential findings

-   Use relatable language, even if it's less exact. No one knows what a
    Census Tract is... say "area" or something like that.
