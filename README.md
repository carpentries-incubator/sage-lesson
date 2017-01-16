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
