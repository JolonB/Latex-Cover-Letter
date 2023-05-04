# Latex-Cover-Letter

A template for a cover letter (or similar) in LaTeX.

This template will not work with pdflatex due to the `\setmainfont` command. This can be removed for full compatibility. Otherwise, it is suggested that you use LuaLaTeX or XeLaTeX.

You can install these with:

```shell
sudo apt install texlive-latex-extra
sudo apt install texlive-luatex
luaotfload-tool --update
```

Try building the sample file with:

```shell
lualatex sample.tex
```

This will require having the Calibri font install on your machine.
You can get it by running the following commands:

```shell
sudo apt install -y ttf-mscorefonts-installer
mkdir ~/.fonts
wget -qO- http://plasmasturm.org/code/vistafonts-installer/vistafonts-installer | bash
rm PowerPointViewer.exe
```
<!--
The installer can also be wget'd from the Internet Archive using the following link: https://web.archive.org/web/20221210114820if_/http://plasmasturm.org/code/vistafonts-installer/vistafonts-installer.
If the PowerPointViewer.exe file has been deleted, it can also be downloaded from the Internet Archive: https://web.archive.org/web/20230504111911/https://cytranet.dl.sourceforge.net/project/mscorefonts2/cabs/PowerPointViewer.exe
 -->

If you don't want to use that font, you can change the font by editing the template file.

## Commands

| Command | Function | Required |
| --- | --- | --- |
| `\setname` | Sets the name of the document author. | &check; |
| `\settopmatter` | Sets additional information, such as contact details. These should be separated by a new line (`\\`). | |
| `\setgreeting` | Sets the introductory sentence. Defaults to "Dear Hiring Manager," if nothing provided. | |
| `\setregarding` | Set the topic of the letter. | |
| `\setfarewell` | Sets the sign off message. Defaults to "Yours faithfully," if nothing provided. | |

In order to use this template, provide any necessary information through the use of the above commands. The body of the cover letter can be contained within:

```latex
\begin{coverletter}
    % Text goes here
\end{coverletter}
```

A sample file is provided [sample.tex](sample.tex). The output is shown below.

![typeset sample file](img/sample.png)
