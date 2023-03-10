# Anotação do genoma da bactéria Clostridium botulinum com pyrodigal e prokka

## Projeto Final do WBDS LA CAMP

Elaborado para WBDSLA, por **Rafaella Pontes Marques**

<p xmlns:dct="http://purl.org/dc/terms/" xmlns:vcard="http://www.w3.org/2001/vcard-rdf/3.0#">
  <a rel="license"
     href="http://creativecommons.org/publicdomain/zero/1.0/">
    <img src="http://i.creativecommons.org/p/zero/1.0/88x31.png" style="border-style: none;" alt="CC0" />
  </a>
  <br />
  To the extent possible under law,
  <a rel="dct:publisher"
     href="https://github.com/rpmarq">
    <span property="dct:title">Rafaella Pontes Marques</span></a>
  has waived all copyright and related or neighboring rights to
  <span property="dct:title">Projeto Final WBDS LA CAMP - Anotação do genoma da bactéria Clostridium botulinum com pyrodigal e prokka </span>.
This work is published from:
<span property="vcard:Country" datatype="dct:ISO3166"
      content="BR" about="https://github.com/rpmarq">
  Brasil</span>.
</p>


O **objetivo** deste projeto é realizar a **anotação do genoma da bactéria Clostridium botulinum utilizando pyrodigal e Prokka**. Adicionalmente, pretende-se realizar uma busca nominal simples com intuito de encontrar genes que codifiquem para algum dos subtipos da toxina botulínica.

- ### **Instalação**- As seguintes bibliotecas, algoritmos e banco de dados serão necessários para as análise:

    - **credentials.py:** arquivo para armazenar chaves de acesso para a API NCBI;
    - **pandas:** para manipulação de dataframes;
    - **pyrodigal:** para a predição de genes codificadores;
    - **requests:** para interagir com a API NCBI;
    - **BioPython:** para manipulação de sequência;
    - [**Galaxy:**](https://usegalaxy.org/) uma plataforma online para análise de sequências biológicas que integra diversos algoritmos, dentre eles o Prokka e o JBrowse:
        - O **Prokka** é um algoritmo de anotação de genomas procariótos;
        - O **JBrowse** é um genome browser (visualizador de genoma) online.
    - [**UniProt:**](https://www.uniprot.org/help/about) é um banco de dados de anotação de proteínas.

- ### **Execução**:

    - O arquivo contendo as comandos utilizados na análise, **"anotacao_cb_script.ipynb"**, encontra-se no diretório **script**. Recomenda-se que este seja visualizado utilizando o [Google Colaboratory](https://colab.research.google.com/);
    - O modelo para preenchimento das informações referentes a chave API do NCBI, **"credentials.py"**, encontra-se no diretório **input**. Você deve preencher com seu email e a chave API gerada na conta NCBI. [Informações sobre chave API](https://support.nlm.nih.gov/knowledgebase/article/KA-05317/en-us)
    - Os arquivos necessários para a análise e os gerados após a execução deste projeto podem ser encontrados nos diretórios **input** e **output**, respectivamente.
    
    - **Arquivos do diretório input:**
        - credential.py;
        - GCF_000827935.1_ASM82793v1_genomic.fna: sequência genômica de *Clostridium botulinum*. Também pode ser obtido acessando a página do assembly [ASM82793v1](https://www.ncbi.nlm.nih.gov/data-hub/genome/GCF_000827935.1/) no site NCBI-Genome.
        
    - **Arquivos do diretório output:**
        - Arquivos gerados pelo algoritmo prodigal:
          - CP010520.1.faa: arquivo contendo as traduções das sequências preditas;
          - CP010520.1.gff: arquivo contendo a anotação das sequências preditas;
          
        - Arquivos gerados pelo algoritmo Prokka do Galaxy:
          - Prokka on data 1: log: arquivo contendo os parâmetros e comandos usados na análise;
          - Prokka on data 1: txt: arquivo contendo um resumo dos resultados;
          - Prokka on data 1: err: arquivo contendo os erros fatais;
          - Prokka on data 1: tsv e Prokka on data 1: tbl: arquivos semelhantes em formato tabular que apresentam o locus genômico, tamanho da sequência, gene e produto gerado;
          - Prokka on data 1: fsa: arquivo contendo a sequência dos contigs;
          - Prokka on data 1: sqn: arquivo contendo as informações da análise e que pode ser submetido ao GenBank;
          - Prokka on data 1: ffn: arquivo contendo as sequências de cDNA das proteínas identificadas;
          - Prokka on data 1: faa: arquivo contendo as sequências de aminoácidos das proteínas identificadas;
          - Prokka on data 1: fna: arquivo contendo a sequência input;
          - Prokka on data 1: gbk: arquivo GenBank contendo as sequências e anotações;
          - Prokka on data 1: gff: arquivo gff contendo as sequências e anotações.
          
        - Arquivos gerados pelo algoritmo JBrowse do Galaxy:
          - JBrowse on data 2 and data 4 - minimal:  um [visualizador do genoma](https://usegalaxy.org/datasets/f9cad7b01a472135f1ad8b380459ee03/display/?preview=True&loc=NZ_CP010520.1%3A1161838..1165596&tracks=DNA%2C39478e4cd0509717a1b5d6108b47bfca_0&highlight=)

## Sobre mim
Meu nome é Rafaella Pontes Marques, sou Graduanda em Biomedicina na Universidade Federal de São Paulo. Contato: rafaella.marques@unifesp.br

