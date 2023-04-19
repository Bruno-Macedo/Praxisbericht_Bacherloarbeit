FROM texlive/texlive:latest

LABEL ba="bachelorarbeit"

USER root

RUN apt-get install texlive texlive-lang-german texlive-latex-extra 
RUN apt-get install texlive-full 

WORKDIR /home/bachelorarbeit
RUN mkdir /home/bachelorarbeit/assets

COPY Bachelorarbeit/assets /home/bachelorarbeit/assets
COPY . /home/bachelorarbeit/

COPY /home/bachelorarbeit/latexcompile /usr/bin/

CMD [ "latexcompile", "-b -r -s -g", "0_bachelorarbeit.tex" ]
