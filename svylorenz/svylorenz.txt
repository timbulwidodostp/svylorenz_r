# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Lorenz curve Use svylorenz (convey) With (In) R Software
install.packages("convey")
install.packages("laeken")
library("convey")
library("survey")
library("laeken")
spml_one = read.csv("https://raw.githubusercontent.com/timbulwidodostp/svylorenz_r/main/svylorenz/svylorenz.csv",sep = ";")
# Estimation Lorenz curve Use svylorenz (convey) With (In) R Software
des_eusilc <- svydesign(ids = ~rb030, strata = ~db040,  weights = ~rb050, data = svylorenz)
des_eusilc <- convey_prep(des_eusilc)
svylorenz(~eqincome, des_eusilc, seq(0,1,.05), alpha = .01)
#
# Lorenz curve Use svylorenz (convey) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished