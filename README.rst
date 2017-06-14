IARC bioinformatics nextflow pipelines
======================================

Nextflow pipelines list
-----------------------

Raw NGS data processing
~~~~~~~~~~~~~~~~~~~~~~~

+--------------+--------------------+--------------------+
| Name         | Description        | Tools used         |
+==============+====================+====================+
| `alignment-n | Performs BAM       | `bwa <https://gith |
| f <https://g | realignment or     | ub.com/lh3/bwa>`__ |
| ithub.com/IA | fastq alignment,   | ,                  |
| RCbioinfo/al | with/without local | `samblaster <https |
| ignment-nf>` | indel realignment  | ://github.com/Greg |
| __           | and base quality   | oryFaust/samblaste |
|              | score              | r>`__,             |
|              | recalibration      | `sambamba <https:/ |
|              |                    | /github.com/lomere |
|              |                    | iter/sambamba>`__  |
|              |                    | & in option:       |
|              |                    | `samtools <http:// |
|              |                    | samtools.sourcefor |
|              |                    | ge.net/>`__,       |
|              |                    | `AdapterRemoval <h |
|              |                    | ttps://github.com/ |
|              |                    | MikkelSchubert/ada |
|              |                    | pterremoval>`__,   |
|              |                    | `GATK <www.broadin |
|              |                    | stitute.org/gatk/d |
|              |                    | ownload>`__,       |
|              |                    | `k8 javascript     |
|              |                    | execution          |
|              |                    | shell <https://sou |
|              |                    | rceforge.net/proje |
|              |                    | cts/bio-bwa/files/ |
|              |                    | bwakit/>`__,       |
|              |                    | `bwa-postalt.js <h |
|              |                    | ttps://github.com/ |
|              |                    | lh3/bwa/tree/maste |
|              |                    | r/bwakit>`__       |
+--------------+--------------------+--------------------+
| `BQSR-nf <ht | Performs base      | `samtools <http:// |
| tps://github | quality score      | samtools.sourcefor |
| .com/IARCbio | recalibration of   | ge.net/>`__,       |
| info/BQSR-nf | bam files using    | `samblaster <https |
| >`__         | GATK               | ://github.com/Greg |
|              |                    | oryFaust/samblaste |
|              |                    | r>`__,             |
|              |                    | `sambamba <https:/ |
|              |                    | /github.com/lomere |
|              |                    | iter/sambamba>`__, |
|              |                    | `GATK <www.broadin |
|              |                    | stitute.org/gatk/d |
|              |                    | ownload>`__        |
+--------------+--------------------+--------------------+
| `abra-nf <ht | Runs ABRA          | `ABRA <https://git |
| tps://github | (Assembly Based    | hub.com/mozack/abr |
| .com/IARCbio | ReAligner)         | a>`__,             |
| info/abra-nf |                    | `bedtools <http:// |
| >`__         |                    | bedtools.readthedo |
|              |                    | cs.io/en/latest/>` |
|              |                    | __,                |
|              |                    | `bwa <http://bio-b |
|              |                    | wa.sourceforge.net |
|              |                    | >`__,              |
|              |                    | `sambamba <http:// |
|              |                    | lomereiter.github. |
|              |                    | io/sambamba/>`__,  |
|              |                    | `samtools <http:// |
|              |                    | www.htslib.org/>`_ |
|              |                    | _                  |
+--------------+--------------------+--------------------+
| `RNAseq-nf < | Performs RNAseq    | `fastqc <http://ww |
| https://gith | mapping, quality   | w.bioinformatics.b |
| ub.com/IARCb | control, and reads | abraham.ac.uk/proj |
| ioinfo/RNAse | counting - See     | ects/fastqc/INSTAL |
| q-nf>`__     | also               | L.txt>`__,         |
|              | `RNAseq\_analysis\ | `cutadapt <http:// |
|              | _scripts <https:// | cutadapt.readthedo |
|              | github.com/IARCbio | cs.io/en/stable/in |
|              | info/RNAseq_analys | stallation.html>`_ |
|              | is_scripts>`__     | _,                 |
|              | for                | Python version >   |
|              | post-processing    | 2.7,               |
|              |                    | `trim\_galore <htt |
|              |                    | ps://github.com/Fe |
|              |                    | lixKrueger/TrimGal |
|              |                    | ore>`__,           |
|              |                    | `RESeQC <http://rs |
|              |                    | eqc.sourceforge.ne |
|              |                    | t/>`__,            |
|              |                    | `multiQC <http://m |
|              |                    | ultiqc.info/docs/> |
|              |                    | `__,               |
|              |                    | `STAR <https://git |
|              |                    | hub.com/alexdobin/ |
|              |                    | STAR/blob/master/d |
|              |                    | oc/STARmanual.pdf> |
|              |                    | `__,               |
|              |                    | `htseq <http://www |
|              |                    | -huber.embl.de/HTS |
|              |                    | eq/doc/install.htm |
|              |                    | l#install>`__      |
|              |                    | & in option:       |
|              |                    | `hisat2 <https://c |
|              |                    | cb.jhu.edu/softwar |
|              |                    | e/hisat2/index.sht |
|              |                    | ml>`__,            |
|              |                    | `GATK <www.broadin |
|              |                    | stitute.org/gatk/d |
|              |                    | ownload>`__,       |
|              |                    | `samtools <http:// |
|              |                    | samtools.sourcefor |
|              |                    | ge.net/>`__        |
+--------------+--------------------+--------------------+
| `GATK-Alignm | Performs bwa       | `bwa <https://gith |
| ent-nf <http | alignment and      | ub.com/lh3/bwa>`__ |
| s://github.c | pre-processing     | ,                  |
| om/IARCbioin | (realignment and   | picard,            |
| fo/GATK-Alig | recalibration)     | `GATK <www.broadin |
| nment-nf>`__ | following GATK     | stitute.org/gatk/d |
|              | best practices     | ownload>`__        |
|              | (less performant   |                    |
|              | than               |                    |
|              | `alignment-nf <htt |                    |
|              | ps://github.com/IA |                    |
|              | RCbioinfo/alignmen |                    |
|              | t-nf>`__           |                    |
|              | )                  |                    |
+--------------+--------------------+--------------------+

QC
~~

+--------------+--------------------+--------------------+
| Name         | Description        | Tools used         |
+==============+====================+====================+
| `conpair-nf  | Runs conpair       | `conpair <https:// |
| <https://git | (concordance and   | github.com/nygenom |
| hub.com/IARC | contamination      | e/Conpair>`__,     |
| bioinfo/conp | estimator)         | `Python            |
| air-nf>`__   |                    | 2.7 <www.python.or |
|              |                    | g>`__,             |
|              |                    | `numpy 1.7.0 or    |
|              |                    | higher <www.numpy. |
|              |                    | org>`__,           |
|              |                    | `scipy 0.14.0 or   |
|              |                    | higher <www.scipy. |
|              |                    | org>`__,           |
|              |                    | `GATK 2.3 or       |
|              |                    | higher <www.broadi |
|              |                    | nstitute.org/gatk/ |
|              |                    | download>`__       |
+--------------+--------------------+--------------------+
| `damage-esti | Runs "Damage       | `Damage            |
| mator-nf <ht | Estimator"         | Estimator <https:/ |
| tps://github |                    | /github.com/Ettwil |
| .com/IARCbio |                    | ler/Damage-estimat |
| info/damage- |                    | or>`__,            |
| estimator-nf |                    | `samtools <http:// |
| >`__         |                    | samtools.sourcefor |
|              |                    | ge.net/>`__,       |
|              |                    | `R <https://www.r- |
|              |                    | project.org>`__    |
|              |                    | with GGPLOT2       |
|              |                    | package            |
+--------------+--------------------+--------------------+
| `bamsurgeon- | Runs bamsurgeon    | `Python            |
| nf <https:// | with step of       | 2.7 <www.python.or |
| github.com/I | variant simulation | g>`__,             |
| ARCbioinfo/b |                    | `bamsurgeon <http: |
| amsurgeon-nf |                    | //github.com/adame |
| >`__         |                    | wing/bamsurgeon/>` |
|              |                    | __,                |
|              |                    | `R                 |
|              |                    | software <https:// |
|              |                    | www.r-project.org/ |
|              |                    | >`__               |
|              |                    | (tested with R     |
|              |                    | version 3.2.3)     |
+--------------+--------------------+--------------------+

Variant calling
~~~~~~~~~~~~~~~

+--------------+--------------------+--------------------+
| Name         | Description        | Tools used         |
+==============+====================+====================+
| `platypus-nf | Runs Platypus      | `Platypus <https:/ |
|  <https://gi | (germline variant  | /github.com/andyri |
| thub.com/IAR | caller)            | mmer/Platypus>`__  |
| Cbioinfo/pla |                    |                    |
| typus-nf>`__ |                    |                    |
+--------------+--------------------+--------------------+
| `GATK-Callin | Runs variant       | `GATK <www.broadin |
| g-GVCF-nf <h | calling in GVCF    | stitute.org/gatk/d |
| ttps://githu | mode on bam files, | ownload>`__        |
| b.com/IARCbi | joint genotyping   |                    |
| oinfo/GATK-C | and variant        |                    |
| alling-GVCF- | recalibration      |                    |
| nf>`__       | (SNPs and indels)  |                    |
|              | following GATK     |                    |
|              | best practices -   |                    |
|              | still in           |                    |
|              | development!!      |                    |
+--------------+--------------------+--------------------+
| `CODEX-nf <h | Performs copy      | `R <https://www.r- |
| ttps://githu | number variant     | project.org>`__    |
| b.com/IARCbi | calling from whole | with package       |
| oinfo/CODEX- | exome sequencing   | Codex, Rscript     |
| nf>`__       | data using CODEX   |                    |
+--------------+--------------------+--------------------+
| `needlestack | Performs           | `perl <https://www |
|  <https://gi | multi-sample       | .perl.org>`__,     |
| thub.com/IAR | somatic variant    | `bedtools <http:// |
| Cbioinfo/nee | calling            | bedtools.readthedo |
| dlestack>`__ |                    | cs.org/en/latest/> |
|              |                    | `__,               |
|              |                    | `samtools <http:// |
|              |                    | samtools.sourcefor |
|              |                    | ge.net/>`__        |
|              |                    | and Rscript        |
+--------------+--------------------+--------------------+
| `mutect-nf < | Runs Mutect on     | `Mutect <https://g |
| https://gith | tumor-matched      | ithub.com/broadins |
| ub.com/IARCb | normal bam pairs   | titute/mutect>`__  |
| ioinfo/mutec |                    | and its            |
| t-nf>`__     |                    | dependencies (Java |
|              |                    | 1.7 and Maven      |
|              |                    | 3.0+),             |
|              |                    | `bedtools <http:// |
|              |                    | bedtools.readthedo |
|              |                    | cs.io/en/latest/co |
|              |                    | ntent/installation |
|              |                    | .html>`__          |
+--------------+--------------------+--------------------+
| `strelka-nf  | Runs Strelka       | `Strelka <https:// |
| <https://git |                    | sites.google.com/s |
| hub.com/IARC |                    | ite/strelkasomatic |
| bioinfo/stre |                    | variantcaller/home |
| lka-nf>`__   |                    | /strelka-workflow- |
|              |                    | installation>`__   |
+--------------+--------------------+--------------------+

Other
~~~~~

+------------------------------------------------------------------------+--------------------------------------------------+---------------------------------------------------+
| Name                                                                   | Description                                      | Tools used                                        |
+========================================================================+==================================================+===================================================+
| `addreplacerg-nf <https://github.com/IARCbioinfo/addreplacerg-nf>`__   | Adds and replaces read group tags in BAM files   | `samtools <http://samtools.sourceforge.net/>`__   |
+------------------------------------------------------------------------+--------------------------------------------------+---------------------------------------------------+

Nextflow
--------

Installation :
~~~~~~~~~~~~~~

1. Install `java <https://java.com/download/>`__ JRE if you don't
   already have it (7 or higher).

2. Install `nextflow <http://www.nextflow.io/>`__.

   .. code:: bash

       curl -fsSL get.nextflow.io | bash

   And move it to a location in your ``$PATH`` (``/usr/local/bin`` for
   example here):

   .. code:: bash

       sudo mv nextflow /usr/local/bin

Configuration file
~~~~~~~~~~~~~~~~~~

Pipelines updates :
~~~~~~~~~~~~~~~~~~~

You can update the nextflow sofware and the pipeline itself simply
using:

.. code:: bash

    nextflow -self-update
    nextflow pull iarcbioinfo/pipeline_name

You can also automatically update the pipeline when you run it by adding
the option ``-latest`` in the ``nextflow run`` command. Doing so you
will always run the latest version from Github.

Display help :
~~~~~~~~~~~~~~

.. code:: bash

    nextflow run iarcbioinfo/pipeline_name --help

Docker
------

Install `docker <https://www.docker.com>`__.

This is very system specific (but quite easy in most cases), follow
`docker documentation <https://docs.docker.com/installation/>`__. Also
follow the optional configuration step called ``Create a Docker group``
in their documentation.

To run nextflow pipeline with Docker, simply add the ``-with-docker``
option.
