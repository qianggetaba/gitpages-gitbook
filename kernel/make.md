explain some make use in kernel makefile

ifeq ($(KBUILD_SRC),)  ; if KBUILD_SRC is empty

ifeq ("$(origin C)", "command line")  ; param C in make commandline like: make C=0

$(filter on%, $(VAR))  ; return all match on% in VAR

$(filter-out on%, $(VAR))  ; return all NOT match on% in VAR

