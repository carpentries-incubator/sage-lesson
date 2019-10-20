This is the lesson on [SageMath](SageMath).

It is being developed for the Software Carpentry workshop at the
[CoDiMa Training School in Computational Discrete Mathematics](http://www.codima.ac.uk/).

If you would like to contribute to the development of this lesson,
please follow the instructions bellow.

## Setup

1. Install [SageMath](SageMath).

## Access the lesson locally

1. Run

   ~~~
   $ make lesson-ipynb serve
   ~~~

   If you don't have SageMath on you `PATH` you **must** run

   ~~~
   $ make lesson-ipynb serve SAGE=/full/path/to/sage
   ~~~

2. Open [http:localhost:4000](http:localhost:4000) on your web browser.

## Change the lesson

1. Launch SageMath by running

   ~~~
   $ sage --notebook=jupyter
   ~~~

2. Open [http://localhost:8888/](http://localhost:8888/) on your web browser.

3. Select the directory `_episodes_ipynb`.

4. Edit the file as you want.

5. To preview the lesson, follow the instructions on ["Access the lesson locally"](#access-the-lesson-locally).

## Sharing your changes

Send a pull request with **only** the changes on `_episodes_ipynb`
to [https://github.com/alex-konovalov/sage-lesson/](https://github.com/alex-konovalov/sage-lesson/).

[SageMath]: http://sagemath.org

## Acknowledgements

We acknowledge financial support from [CCP-CoDiMa](https://www.codima.ac.uk/)
(Collaborative Computational Project in the area of Computational Discrete Mathematics
[EP/M022641/1](http://gow.epsrc.ac.uk/NGBOViewGrant.aspx?GrantRef=EP/M022641/1))
and from [OpenDreamKit](http://opendreamkit.org/) [Horizon 2020](https://ec.europa.eu/programmes/horizon2020/)
[European Research Infrastructures](https://ec.europa.eu/programmes/horizon2020/en/h2020-section/european-research-infrastructures-including-e-infrastructures)
project (#<a href="http://cordis.europa.eu/project/rcn/198334_en.html">676541</a>).


