* 2017-03-6 21:00, Yu-jian Kang

Here is a temporary package of CPC2.


1) Pre-requisite:

a. Biopython package: a local version could be downloaded from
http://biopython.org/wiki/Download

2) Install

a. Unpack the tarball:

tom@linux$ gzip -dc CPC2-beta.tar.gz | tar xf -

b. Build third-part packages: 

tom@linux$ cd CPC2-beta
tom@linux$ export CPC_HOME="$PWD"
tom@linux$ cd libs/libsvm
tom@linux$ gzip -dc libsvm-3.18.tar.gz | tar xf -
tom@linux$ cd libsvm-3.18
tom@linux$ make clean && make

3) Run the predict

tom@linux$ cd $CPC_HOME
tom@linux$ bin/CPC2.py -i (input_seq) -o (result_in_table)

example:
tom@linux$ bin/CPC2.py -i data/example.fa -o example_output

4) Output result

Result in table format (delimited by tab):
#ID	peptide_length	Fickett_score	isoelectric_point	ORF_integrity	coding_probability	coding_label


	See the website for tutorial and more details. (http://cpc2.cbi.pku.edu.cn)

	This is a beta version of CPC2, if have any questions please report to us.

	Contact: cpc@mail.cbi.pku.edu.cn
