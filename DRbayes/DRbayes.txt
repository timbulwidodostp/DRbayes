# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Doubly robust estimates of causal effects in high-dimensions using flexible Bayesian methods Use DRbayes (DoublyRobustHD) With (In) R Software
install.packages("remotes")
remotes::install_github("jantonelli111/DoublyRobustHD")
library("DoublyRobustHD")
# Estimate Doubly robust estimates of causal effects in high-dimensions using flexible Bayesian methods Use DRbayes (DoublyRobustHD) With (In) R Software
DRbayes = read.csv("https://raw.githubusercontent.com/timbulwidodostp/DRbayes/main/DRbayes/DRbayes.csv",sep = ";")
y <- DRbayes$y
t <- DRbayes$t
X1 <- DRbayes$X1
X2 <- DRbayes$X2
X3 <- DRbayes$X3
x <- cbind(X1, X2, X3)
x_ <- cbind(X1, X2)
DRbayes = DRbayes(y = y, t = t, x = x, nScans = 20, nBurn = 10, thin = 2)
DRbayes_ = DRbayes(y = y, t = t, x = x_, nScans = 20, nBurn = 10, thin = 2)
DRbayes
DRbayes_
# Doubly robust estimates of causal effects in high-dimensions using flexible Bayesian methods Use DRbayes (DoublyRobustHD) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished