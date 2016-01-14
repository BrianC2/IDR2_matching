# Work Flow Chart

##EYEBALL EXAMPLE
##Input your choices into eyeball_choices.txt
##Look in /media/brian/Data/Documents/University/3_Third_Year/Summer_Semester/SCIE30001/IDR2_matching/PLOTS/plotting_scripts
##and look at extended plots in one window:
cd /media/brian/Data/Documents/University/3_Third_Year/Summer_Semester/SCIE30001/IDR2_matching/PLOTS/plotting_scripts
eog *extended*png
##in another window, look at pumaplots:
eog *pumaplot*png
##make choices as the following
a c = accept PUMA's decision to combine
a 1 = accept the combination labelled 1 (agree with PUMA's decision)
      works for any number i.e. combo 2,3
c = diagree with PUMA, combine EVERYTHING in the pumaplot
1 = disagree with PUMA, select specific combination (also for 2,3
    etc)
r = disagree with PUMA, manual edit due to specific combinaiton
    needed, or extra source needed
##As you go along, make notes on any r, c or number as to why
##you disagreed with PUMA
##ALSO, note down names of sources with mental spectral behaviour

##Once done, run this command:
source use_choices.sh
##This will create:
eyeball_deep_choices.vot 
eyeball_deep_reject_list.txt  
eyeball_deep_reject_pile.txt
eyeball_multi_choices.vot 
eyeball_multi_reject_list.txt
eyeball_multi_reject_pile.txt

##Want to copy files like this:
cp eyeball_deep_reject_list.txt eyeball_deep_reject_choices.txt
cp eyeball_multi_reject_list.txt eyeball_multi_reject_choices.txt
cp eyeball_deep_reject_pile.txt eyeball_deep_reject_pile_mod.txt
cp eyeball_multi_reject_pile.txt eyeball_multi_reject_pile_mod.txt

##Then check your initial decision using plot_edit.sh in 
cd /media/brian/Data/Documents/University/3_Third_Year/Summer_Semester/SCIE30001/IDR2_matching/PLOTS/plotting_scripts

##Now work through all of the manual rejects. If you need
##to edit the sources to be included, add/remove them between
##START_GROUP and START_COMP
##Source information goes:
##catalogue name ra error_ra dec error_dec frequency flux error_flux -things-you-dont-care-about
##If you want to combine all that is left, in the choice file type
all
##If you want a specific combination of sources, list their names
##separated by commas e.g. 
J002619-150423 J002615-150422,002623-150405





##GIT STUFF==================

##Update a file using git:
git add *name of file/s* e.g. git add use_choices.py etc etc
git commit -m "Comment regarding this commit" e.g. git commit -m "Brian's first commit"
git push (then enter user name and password)


##Set your git settings to be slightly conservative rather than aggresive
git config --global push.default simple

##Change the fork of your local repository to the designated fork
git remote set-url origin https://github.com/BrianC2/IDR2_matching.git

##Retrieve 
git clone https://github.com/BrianC2/IDR2_matching.git

git remote set-url origin https://github.com/JLBLine/IDR2_matching.git
