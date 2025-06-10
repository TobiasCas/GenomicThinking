# GenomicThinking
code for genimic thinking course

removing dunius gender
plink --bfile gwas_data --check-sex --out gwas_data
head gwas_data.sexcheck
grep -v "OK" gwas_data.sexcheck > wrong_sex.txt
plink --bfile gwas_data --remove wrong_sex.txt --make-bed --out gwas_QC
