# æthel
A repository for æthel, a dataset of Intuitionistic Linear Logic theorems, automatically 
extracted from the Lassy Small corpus.
Read more about the dataset in our LREC [paper](http://www.lrec-conf.org/proceedings/lrec2020/pdf/2020.lrec-1.647.pdf).

The latest version of the dataset contains mechanically verified analyses for 73.331 sentences 
(58.913 train / 7.207 dev / 7.211 test), and can be downloaded 
[here](https://surfdrive.surf.nl/files/index.php/s/zHEgwDJQ7jxnpCI),
in the form of a serialized Python file.
Please refer to [this](https://github.com/konstantinosKokos/Lassy-TLG-Extraction/) repository for a quickstart guide.

The `lexicon` directory of this repository contains corpus-wide aggregated frequency information.
## updates
* 22/01/2021: (*0.4.dev0*) improvements to the type grammar (modalities are now unary), pretty printing, explicit 
  type-checking of terms
* 07/12/2020: switching from the .xml format to the binarized proof net format. The natural deduction and sequent calculus presentation of the previous dataset version can be found in the [old](https://github.com/konstantinosKokos/aethel/tree/old) branch.  
* 29/08/2020: the **full** dataset is now open access.
* 29/10/2019: released the wiki subset of the dataset. 

## contact
If you encounter any issues, find any inconsistencies, or just need help getting started, do not hesitate to get in touch.
