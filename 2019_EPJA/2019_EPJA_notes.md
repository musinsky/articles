All LaTeX files and figures received at 2021-03 from Egle.

## EPJA history
* 2019-08-16 submission ALPOM manuscript EPJA-105322 (and at the same time arXiv:1908.06159)
* 2019-09-26 EPJA-105322 comments from referees
* 2019-11-02 submit revision EPJA-105322.R1
* 2019-11-26 EPJA-105322.R1 manuscript has been accepted for publication
* 2020-01-28 published online

## LaTeX
EPJA-105322 manuscript (`ALPOM.tex` size 63749 bytes, 2019-08-16). This version is on [arXiv.org](https://arxiv.org/abs/1908.06159) with minimum modification (arXiv.org changes all figures to `*.pdf`). Source files and pdf file from https://arxiv.org/abs/1908.06159 and https://arxiv.org/abs/1908.06159v1 are absolutely identically ?!

Revision EPJA-105322.R1 manuscript (`ALPOMRev.tex` size 65515 bytes, 2019-10-30) has been accepted for publication. This file is stored. Modifications in file come only with LaTeX (formatting, cleaning, etc.) and original text is **UNTOUCHED**.

Submitted EPJA manuscript LaTeX file contained very obsolete template files from [EPJA_templ.zip](https://mc.manuscriptcentral.com/societyimages/epja/EPJA_templ.zip)
* `svjour.cls` SVJour DOCUMENT CLASS -- version 1.11 for LaTeX2e (2003/04/15)

and was replaced by actual template files from [svjour3-epj_a_c.zip](http://epj.org/images/stories/latex/svjour3-epj_a_c.zip)
* `svjour3.cls` SVJour3 DOCUMENT CLASS -- version 3.3 for LaTeX2e (2010/11/25)

## Figures
Some figures are in raster format (jpg/png) and encapsulated in vector format (pdf/eps). This causes unnecessary confusion.

* `fig01_gepgmp.pdf` vector (original `gepgmp_allpol_final_lin_lin.pdf` vector)
```
qpdf --rotate=-90 gepgmp_allpol_final_lin_lin.pdf - | pdfcrop - fig01_gepgmp.pdf
```
* `fig02_gengmn.pdf` vector (original `gengmn.pdf` vector)
```
pdfcrop gengmn.pdf fig02_gengmn.pdf
```
* `fig03_A_Y_Comb1a.pdf` vector (original `A_Y_Comb1a.pdf` vector)
```
pdfcrop A_Y_Comb1a.pdf fig03_A_Y_Comb1a.pdf
```
* `fig04_npPol3.pdf` vector (original `npPol3.pdf` vector)
```
pdfcrop npPol3.pdf fig04_npPol3.pdf
```
* `fig05_ALPOM_Fig3b.pdf` vector (original `ALPOM-Fig3b.pdf` vector)
```
pdfcrop ALPOM-Fig3b.pdf fig05_ALPOM_Fig3b.pdf
```
* `fig06_NeutronFoM1.pdf` vector (original `NeutronFoM1.pdf` vector)
```
pdfcrop NeutronFoM1.pdf fig06_NeutronFoM1.pdf
```
* `fig07_ALPOM2SetUp.png` raster (original `ALPOM2SetUp.pdf` raster in vector)
```
pdfimages -all ALPOM2SetUp.pdf ALPOM2SetUp
convert ALPOM2SetUp-000.png -trim fig07_ALPOM2SetUp.png   # convert (8-bit sRGB 73312B) => (8-bit Gray 256c 38090B)
```
* `fig08_p_beam_375.jpg` raster (original `p_beam_375.jpg` raster)
```
convert p_beam_375.jpg -trim -resize 600x -quality 85 fig08_p_beam_375.jpg
```
* `fig08_n_beam_375.jpg` raster (original `n_beam_375.eps` raster+vector in vector)
```
gs -dBATCH -dNOPAUSE -dSAFER -sDEVICE=jpeg -dJPEGQ=100 -r300 -dEPSCrop -sOutputFile=n_beam_375_q100_r300.jpg n_beam_375.eps
convert n_beam_375_q100_r300.jpg -trim -resize 600x -quality 85 fig08_n_beam_375.jpg
```
* `fig09_cal_375_CH2left.pdf` vector (original `cal_375_CH2left.eps` vector)
```
cat cal_375_CH2left.eps | epstopdf --filter | pdfcrop - fig09_cal_375_CH2left.pdf
```
* `fig09_cal_60_CH2right.pdf` vector (original `cal_60_CH2right.eps` vector)
```
cat cal_60_CH2right.eps | epstopdf --filter | pdfcrop - fig09_cal_60_CH2right.pdf
```
* `fig10_HadCalDesign.png` raster (original `HadCalDesign.pdf` raster in vector)
```
pdfimages -all HadCalDesign.pdf HadCalDesign
convert HadCalDesign-000.png -trim -resize 800x fig10_HadCalDesign.png
```
* `fig11_Fig11.jpg` raster (original `Fig11.eps` raster in vector)
```
cat Fig11.eps | epstopdf --filter | pdfimages - -all Fig11
convert Fig11-000.jpg -crop 0x0-40+0 -trim fig11_Fig11.jpg
```
* `fig12_Fig12.jpg` raster (original `Fig12.pdf` raster+vector in vector)
```
gs -dBATCH -dNOPAUSE -dSAFER -sDEVICE=jpeg -dJPEGQ=100 -r1200 -sOutputFile=Fig12.jpg Fig12.pdf
convert Fig12.jpg -trim -resize 800x -quality 85 fig12_Fig12.jpg
# other options
# pdfimages -all Fig12.pdf Fig12   # create 4 separate high quality png images
# LibreOffice Draw: Export As PDF: JPEG compression Quality 75%, Reduce image resolution 150 DPI
                                   => create ~250kB very well quality image
```
* `fig13_pol_F3.pdf` vector (original `pol_F3.eps` vector)
```
cat pol_F3.eps | epstopdf --filter | pdfcrop - fig13_pol_F3.pdf
```
* `fig14_nC_pt2.pdf`vector (original `nC_pt2.eps` vector)
```
cat nC_pt2.eps | epstopdf --filter | pdfcrop - fig14_nC_pt2.pdf
```
* `fig15_pCH2_pt2.pdf` vector (original `pCH2_pt2.eps` vector)
```
cat pCH2_pt2.eps | epstopdf --filter | pdfcrop - fig15_pCH2_pt2.pdf
```
* `fig16_control_meas.pdf` vector (original `control_meas.eps` vector)
```
cat control_meas.eps | epstopdf --filter | pdfcrop - fig16_control_meas.pdf
```
* `fig17_hadcal_asym.pdf` vector (original `hadcal_asym_corr.eps` vector)
```
cat hadcal_asym_corr.eps | epstopdf --filter | pdfcrop - fig17_hadcal_asym.pdf
```
* `fig18_nCH2_3-42.pdf` vector (original `nCH2_3-42.eps` vector)
```
cat nCH2_3-42.eps | epstopdf --filter | pdfcrop - fig18_nCH2_3-42.pdf
```
* `fig18_nAll_375.pdf` vector (original `nAll_375.eps` vector)
```
cat nAll_375.eps | epstopdf --filter | pdfcrop - fig18_nAll_375.pdf
```
* `fig19_p_n_Cu_hadcal.pdf` vector (original `p_n_Cu_hadcal.eps` vector)
```
cat p_n_Cu_hadcal.eps | epstopdf --filter | pdfcrop - fig19_p_n_Cu_hadcal.pdf
```
