# Assembly-error
Methods and notes on how to detect assembly errors in long molecule based assemblies

The pipeline described here helps to find putative assembly errors. This is especially helpful when variants present in a genome are being validated or assemblies are being merged using <i><a href="https://github.com/mahulchak/quickmerge">quickmerge</a></i>. The method of putative error detection is simple and has been used many.

1. First, obtain the genomic intervals you want to examine for assembly errors. This can be created using bedtools makewindows or it can come from quickmerge output.

2. Align the long reads to your assembly using <i>blasr</i>. Get the output in m1 format and then filter the format following the directions given <a href="https://github.com/mahulchak/proberead">here</a>. We will be using <i>proberead</i> to get the coverage for the intervals.

3. Obtain the coverage of the genomic intervals from the filtered m1 file using <i><a href="https://github.com/mahulchak/proberead">proberead</a></i>

