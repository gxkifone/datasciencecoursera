datasciencecoursera
===================

This is my very first repo that is used for Data Scientist Toolkit from Courera

Really? This is all you've got? 



#remove classes with less than n instannce

rmMinority <- function(df,y,n=10) {
  y <- substitute(y)
  tbl <- table(eval(y,df))
  nm <- names(tbl[tbl<n])
  df %>% filter(!eval(y,df) %in% nm)
  
}
