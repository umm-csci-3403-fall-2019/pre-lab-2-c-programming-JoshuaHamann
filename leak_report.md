# Leak report

#The memory error happens due to the saved characters when a function is calling on the strip method. In order to fix this error one must delete these saved characters once they are used for their purpose. I.e. strip is used in the function clean and after clean uses these saved characters, we should free() the saved characters since we no longer need them to help keep memory free (we have to do our own garbage collecting)

