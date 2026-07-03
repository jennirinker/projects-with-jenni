.. _final_report:

Final report
===============


I recommend you re-read Lars Landberg's book before beginning to write your thesis to refamiliarize yourself with what a censor is looking for.

The report is handed in as a PDF on CampusNet.

Choosing a structure
--------------------------

There are generally two options for report structure: monograph or compendium.

* **Monograph**. "Classic" report structure. One cohesive document.  
* **Compendium**. Uncommon for MSc theses, more common for PhD theses. Useful if you want to try to publish a paper from your MSc. A chapter in the compendium is a fully prepared draft of a conference or journal paper.

You may choose whichever structure suits your interests.
I'm always interested in publications, so I like when students choose compendiums, but not all projects are well-suited to that format.
If you're interested in a compendium, discuss it with me at least one month before your deadline.


Monograph
------------------

Below is an example of a monograph report structure.
You can change the structure if it better tells your story.
See references in :ref:`scientific_writing` for more details.

1. **Background**. What is the problem you are trying to solve? How have other people solved the problem/related problems? If this is a thesis, what are your research questions and why? 
2. **Methodology**. What technique(s) did you use to solve the problem that the reader needs to know?    
3. **Results**. How well did your technique work? Are there some areas where it doesn't work well? Why?
4. **Discussion**. Summarize the key assumptions, limitations and potential impact of your techniques.  
5. **Conclusion**. Summarize the problem, proposed solution and results. If this is a thesis, write the answers to your research questions based on your results/analysis.

Examples of monographs
""""""""""""""""""""""""""

* BSc. `Theo's thesis <https://findit.dtu.dk/en/catalog/6792e87c64d5f915d2cca087>`_
* MSc. `Esther's thesis <https://findit.dtu.dk/en/catalog/64ab4c8ec3a23191526c38dd>`_
* MSc. `Thea's thesis <https://findit.dtu.dk/en/catalog/612f5fb6d9001d017237203a>`_


Compendium
------------------

Compendiums are non-traditional for MSc theses but give the student experience in writing a scientific paper ready for submission.
Care must be taken in the introduction to orient the reader as to the structure, and section introductions should be used to tell the story throughout the thesis.
See a good example below.

If you want to do a compendium, you and I need to align closely on the content of the paper and the target journal/conference.
Talk to me at least 1 month before you hand in so we can discuss whether a compendium is possible for your project.


Example of compendium
""""""""""""""""""""""""""

Frederik did his thesis with me in 2025, and I think he did a nice job formulating his thesis as a compendium.
He was able to publish his results as a first-author paper as part of the 2026 Torque Conference.

* `Frederik's compendium thesis <https://findit.dtu.dk/en/catalog/6926534a27387d7ce8506230>`_  
* `Frederik's Torque paper <https://iopscience.iop.org/article/10.1088/1742-6596/3224/4/042003>`_

Frederik's thesis worked well as a compendium due to the following elements:  

1. Compendium format explained in outline.  

  * In Section 1.4, Outline, he clearly explains that Section 3 includes a draft paper prepared for the Torque conference.  

2. Paper draft is proceeded by a few paragraphs summarizing context and main conclusions of the paper.  

  * In Section 3, he begins by setting the context of the paper, namely by summarizing the objective and conclusion. He then reiterates that the draft paper follows, and notes potential redundancies with references and citations.  

3. Draft paper is formatted differently than rest of thesis.

  * Frederik prepared the draft paper in a separate LaTeX document using the LaTeX style file provided by the conference, making it slightly visually different than the main thesis.  
  * The draft paper is included in the main thesis LaTeX using the code below. NB: The pages of the draft paper PDF were manually incremented to match the page numbers of the main thesis.  

.. code-block:: latex

   \subsection{Torque 2026 draft paper} 
   The complete draft paper follows on the next page.
   Note that all references and citations within the draft paper refer to figures, tables, equations, and references included in the paper itself.
   Some numbering may overlap with that used in the rest of the thesis, so this should be kept in mind when reading.

   \setcounter{tocdepth}{3}
   \addtocontents{toc}{%
     \protect\contentsline{subsubsection}{\numberline{3.3.1}Introduction}{24}{}}
   \addtocontents{toc}{%
     \protect\contentsline{subsubsection}{\numberline{3.3.2}Methodology}{25}{}}
   \addtocontents{toc}{%
     \protect\contentsline{subsubsection}{\numberline{3.3.3}Results}{27}{}}
   \addtocontents{toc}{%
     \protect\contentsline{subsubsection}{\numberline{3.3.4}Discussion}{32}{}}
   \addtocontents{toc}{%
     \protect\contentsline{subsubsection}{\numberline{3.3.5}Conclusion}{33}{}}
   \includepdf[
       pages=-, 
       pagecommand=\thispagestyle{fancy},
       offset=0cm 0.8cm
   ]{Subfiles/3 - Lidar-derived profiles/Torque_2026_draft_paper.pdf}