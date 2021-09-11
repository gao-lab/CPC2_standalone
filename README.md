CPC2 standalone
====

* 2020-01-13 14:58, Yu-jian Kang
* This is a python 2 verison of CPC2 (same with the version of the original paper).
* Thanks for helps from **HyperOdin**, there is a python 3 version (the release of *CPC2_standalone_python3 v1.0.1*)

1 Pre-requisite:
----
a. Biopython package: a local version could be downloaded from
http://biopython.org/wiki/Download

2 Install
----
a. Unpack the tarball:

	tom@linux$ gzip -dc CPC2-beta.tar.gz | tar xf -

b. Build third-part packages: 

	tom@linux$ cd CPC2-beta
	tom@linux$ export CPC_HOME="$PWD"
	tom@linux$ cd libs/libsvm
	tom@linux$ gzip -dc libsvm-3.18.tar.gz | tar xf -
	tom@linux$ cd libsvm-3.18
	tom@linux$ make clean && make

3 Run the predict
----
	tom@linux$ cd $CPC_HOME
	tom@linux$ bin/CPC2.py -i (input_seq) -o (result_in_table)
	
Example:
	
	tom@linux$ bin/CPC2.py -i data/example.fa -o example_output
	
If you want to output predicted peptide sequence, use CPC2_output_peptide.py with "--ORF" option:

	tom@linux$ bin/CPC2_output_peptide.py -i data/example.fa -o example_output --ORF

4 Output result
----
Result in table format (delimited by tab):<br>
#ID	peptide_length	Fickett_score	isoelectric_point	ORF_integrity	coding_probability	coding_label

Contact
----
>See the website for tutorial and more details. (http://cpc2.cbi.pku.edu.cn)<br>

>This is a beta version of CPC2, if have any questions please report to us.<br>

>Contact: cpc@mail.cbi.pku.edu.cn
