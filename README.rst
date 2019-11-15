|CyVerse logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

QIIME2 Jupyter Lab 
==================

Goals
-----

`QIIME 2™ <https://qiime2.org/>`_ is a next-generation microbiome bioinformatics platform that is extensible, free, open source, and community developed. 

- Automatically track your analyses with decentralized data provenance — no more guesswork on what commands were run!

- Interactively explore your data with beautiful visualizations that provide new perspectives.

- Easily share results with your team, even those members without QIIME 2 installed.

- Plugin-based system — your favorite microbiome methods all in one place.

In this quick start, we will show you how to launch JupyterLab-QIIME2 VICE app in DE

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/9AT2YHkduz0" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>

-----

Prerequisites
-------------

Downloads, access, and services
```````````````````````````````

*In order to complete this tutorial you will need access to the following services/software*

	.. list-table::
	    :header-rows: 1

	    * - Prerequisite
	      - Preparation/Notes
	      - Link/Download
	    * - CyVerse account
	      - You will need a CyVerse account to complete this exercise
	      - `Register <https://user.cyverse.org/>`_

----

Platform(s)
``````````

*We will use the following CyVerse platform(s):*

.. list-table::
    :header-rows: 1

    * - Platform
      - Interface
      - Link
      - Platform Documentation
      - Learning Center Docs
    * - Discovery Environment
      - Web/Point-and-click
      - `Discovery Environment <https://de.cyverse.org/de/>`_
      - `DE Manual <https://wiki.cyverse.org/wiki/display/DEmanual/Table+of+Contents>`_
      - `Guide <https://learning.cyverse.org/projects/discovery-environment-guide/en/latest/>`__

----

Input and example data
``````````````````````

*In order to complete this quickstart you will need to have the following inputs prepared*

.. list-table::
    :header-rows: 1

    * - Input File(s)
      - Format
      - Preparation/Notes
      - Example Data
    * - Sequencing reads
      - `FastQ <https://en.wikipedia.org/wiki/FASTQ_format>`_
      - Any sequencing reads in FastQ format will work. They do not
        need to be pre-processed. They may also be compressed (e.g.
        fastq.gz)
      - gut microbiome (iplantcollaborative > example_data > qiime2  and select gut-microbiome folder)

-----

**Get started**
---------------

1. Login to the |discovery_enviornment|.

2. Click badge |QIIME2|_ to log into CyVerse and view the App.

3. Under “Parameters” for ‘Input folder' or 'Input files', click Browse, then navigate to and
   select one or more FastQ files to analyze; Then click OK.

   .. Note::

	    To use our example data, navigate to *Community Data >*
	    *iplantcollaborative > example_data > qiime2  and select gut-microbiome folder.*

4. Click **Launch Analysis**. You will receive a notification that the job has been submitted and running with the "Access your running analysis here". 

5. Clicking on the "Access your running analysis" will open the JupyterLab-QIIME2 in another tab in the browser after a brief building phase.

.. Note::

  You will be asked to authenticate again to the JupyterLab with your CyVerse username and password

6. You will see the input data under "vice" folder of the JuptyerLab. Now you can upload your own Jupyter Notebook or create one using one of the available kernels

.. warning::

  Do not create or store any outputs inside the input folder (gut-microbiome) as those outputs are not brought back after the analysis

7. Finally, once you finish analysis, navigate to the DE tab, select the Analysis window and select the analysis, click "save and complete analysis". Upon clicking complete analysis, the analysis will be completed and all the outputs will be brought back to the analysis folder.

----

.. note :: 
	UPDATE: Newest version QIIME-2019.10

	The latest version (currently v2019.10 as of 11/8/2019) for QIIME2 in VICE has the capabilities for in-line visualizations in the jupyter notebook.

.. raw:: html

   <div style="position: relative; padding-bottom: 56.25%; height: 0;"><iframe src="https://www.loom.com/embed/7c20c565bf0e490084cfb8e4b62bfb63" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>



Simply import the qiime2 module into the python notebook:

.. code-block:: python

   import qiime2

And use the following command to view your .qzv files in-line with your jupyter notebook:

.. code-block:: python

   qiime2.Visualizations.load('demux.qzv')


This provides all of the perks of using view.qiime2.org to visualize your .qzv files, but you don't need to change tabs. Additionally, everything is kept in the notebook which can be used as a lab notebook or for reproducibility.

**IMPORTANT**: Save all needed output files in the vice directory. Files not in the vice directory will not be retained in your data store analyses folder.

----

Additional information, help
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
- Full materials for the webinar is available `here <https://wiki.cyverse.org/wiki/display/Events/FFW%3A+Doing+metagenomic+analyses+with+QIIME+2+using+Jupyter+Notebooks+in+VICE>`_

- See the original `JupyterLab quick start <https://learning.cyverse.org/projects/vice/en/latest/user_guide/quick-jupyter.html>`_ 

- See the original `qiime2.org <https://qiime2.org>`_ for how to run qiime2 analysis

- Search for an answer: `CyVerse Learning Center <http://learning.cyverse.org>`_ or `CyVerse Wiki <https://wiki.cyverse.org>`_

- Contact CyVerse support by clicking the intercom button on the page.

----

**Fix or improve this documentation**

- On Github: `Repo link <https://github.com/CyVerse-learning-materials/fastqc_quickstart>`_
- Send feedback: `Tutorials@CyVerse.org <Tutorials@CyVerse.org>`_

----

.. |QIIME2| image:: https://de.cyverse.org/Powered-By-CyVerse-blue.svg
.. _QIIME2: https://de.cyverse.org/de/?type=quick-launch&quick-launch-id=0fe69a8f-216d-4103-abd8-a2080af82876&app-id=58150fe4-01cf-11ea-8c41-008cfa5ae621

|Home_Icon|_
`Learning Center Home`_

.. |CyVerse logo| image:: ./img/cyverse_cmyk.png
    :width: 500
.. _CyVerse logo: http://learning.cyverse.org/
.. |Home_Icon| image:: ./img/homeicon.png
    :width: 25
    :height: 25
.. _Home_Icon: http://learning.cyverse.org/
.. |discovery_enviornment| raw:: html

    <a href="https://de.cyverse.org/de/" target="_blank">Discovery Environment</a>

.. |QIIME2| image:: https://de.cyverse.org/Powered-By-CyVerse-blue.svg
.. _QIIME2: https://de.cyverse.org/de/?type=quick-launch&quick-launch-id=0fe69a8f-216d-4103-abd8-a2080af82876&app-id=58150fe4-01cf-11ea-8c41-008cfa5ae621
