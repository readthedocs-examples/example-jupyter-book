Example: Jupyter Book for Read the Docs
=======================================

.. image:: https://readthedocs.org/projects/example-jupyter-book/badge/?version=latest
    :target: https://example-jupyter-book.readthedocs.io/
    :alt: Documentation Status

.. This README.rst should work on GitHub and is also included in the Sphinx documentation project in docs/ - therefore, README.rst uses absolute links for most things so it renders properly on GitHub

This example shows a Jupyter Book project with Read the Docs. You're encouraged to view it to get inspiration and copy & paste from the files in the source code. If you are using Read the Docs for the first time, have a look at the official `Read the Docs Tutorial <https://docs.readthedocs.io/en/stable/tutorial/index.html>`__. If you are using Jupyter Book for the first time, have a look at the `official Jupyter Book documentation <https://jupyterbook.org/en/stable/>`_.

📚 `docs/ <https://github.com/readthedocs-examples/example-jupyter-book/blob/main/docs/>`_
    A basic Jupyter Book project lives in ``docs/``. All the ``*.md`` make up sections in the documentation, ``intro.md`` is the starting page and includes this ``README.rst``.
⚙️ `.readthedocs.yaml <https://github.com/readthedocs-examples/example-jupyter-book/blob/main/.readthedocs.yaml>`_
    Read the Docs Build configuration is stored in ``.readthedocs.yaml``.
⚙️ `docs/_config.yml <https://github.com/readthedocs-examples/example-jupyter-book/blob/main/docs/_config.yml>`_
    This is the `configuration for Jupyter Book <https://jupyterbook.org/en/stable/customize/config.html>`_ which is used to generate a Sphinx-configuration on-the-fly. However, the Sphinx ``conf.py`` file is NOT managed in a git repository, as it is managed by Jupyter Book!
📍 `docs/requirements.txt <https://github.com/readthedocs-examples/example-jupyter-book/blob/main/docs/requirements.txt>`_
    These dependencies need to be installed for Jupyter Book to work. If you are familiar with Python, you might notice that the dependencies are *not* `pinned <https://docs.readthedocs.io/en/latest/guides/reproducible-builds.html>`_. This is the default method for Jupyter Book - on one hand it gives you the latest version each time Read the Docs builds your documentation; but on the other hand, your build can fail in the future if an incompatible version of ``jupyter-book`` is released.
💡 Extension: `Intersphinx <https://docs.readthedocs.io/en/stable/guides/intersphinx.html>`_
    Using this extension, we refer directly to sections in other projects that use Sphinx.
💡 Extension: `sphinx-hoverxref <https://sphinx-hoverxref.readthedocs.io/>`__
    A floating window (also known as a "tooltip" or "modal dialogue") appears when the mouse curser hovers a cross references to another section of the documentation or another documentation project referenced with Intersphinx.
🔢 Simplified versioning
    In this example, we maintain a single version of the rendered documentation by automatically building and rendering everything that is added to the ``main`` branch. This is different from many software projects where several `versions of the docs <https://docs.readthedocs.io/en/stable/versions.html>`_ may be published for each new release.
🔢 Pull Request builds
    Every time a change in a Pull Request on the GitHub repository happens, users can open `an automatically built Pull Request preview <https://docs.readthedocs.io/en/stable/pull-requests.html>`__.
⁉️ Questions / comments
    If you have questions related to this example, feel free to can ask them as a GitHub issue `here <https://github.com/readthedocs-examples/example-jupyter-book/issues>`_.


Example Project usage
---------------------

This project has a standard Jupyter Book layout which is built by Read the Docs almost the same way that you would build it locally (on your own laptop!).

You can build and view this documentation project locally - we recommend that you activate `a local Python virtual environment first <https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment>`_:

.. code-block:: console

    # Install required Python dependencies (Sphinx etc.)
    pip install -r docs/requirements.txt

    # Run Jupyter Book
    jupyter-book build docs/
    
    # View the docs with for instance firefox
    firefox docs/_build/html/index.html


Using the example in your own project
-------------------------------------

If you are new to Read the Docs, you may want to refer to the `Read the Docs User documentation <https://docs.readthedocs.io/>`_.

If you are copying this code in order to get started with your documentation, you need to:

#. use your existing project repository or create a new repository on GitHub, GitLab, Bitbucket or another host supported by Read the Docs
#. copy ``.readthedocs.yaml`` and the ``docs/`` folder into your project.
#. if you want to have a README on GitHub, create a ``README.rst`` which will be included in ``intro.md``.
#. if you *do not* want your README from GitHub included in the docs, edit ``intro.md`` and remove the ``eval-rst`` block that includes it.
#. if you don't already have a ``.gitignore``, use the one from the project file -- otherwise add these lines::

    /docs/conf.py
    /docs/_build

#. customize all the files, replacing example contents.
#. rebuild the documenation locally to see that it works.
#. *finally*, register your project on Read the Docs, see `Importing Your Documentation <https://docs.readthedocs.io/en/stable/intro/import-guide.html>`_.


Read the Docs Tutorial
----------------------

To get started with Read the Docs, you may also refer to the `Read the Docs Tutorial <https://docs.readthedocs.io/en/stable/tutorial/>`__.
It provides a full walk-through of building an example project similar to the one in this repository.
