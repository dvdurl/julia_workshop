### Staring up Julia
Right now I have saved the collection of modules that are required to run Julia on our cluster (linux-based) with Compute alliange framework.
Just by doing ```module load StdEnv/2020 julia/1.8.5``` and ```module save my_julia``` on the terminal, we have load and save the modules required to run Julia in a module collection called ```my_julia```; with this we can just call the module collection when we start a new session by running the *module subcommand* ```restore my_julia```. We can skip this steps by different methods (e.g. environments, alias) - I will create an alias with the module collection and add it to my *bash_aliases* file: ```alias julia_col='module restore my_julia && julia'``` but the alias can be focused on loading the modules instead. Now we can just run the julia command on the terminal and start working.
___

### Setup Project Environments

By running julia_col, we are welcomed with Julia's front message, and since we want to initialize a project we will be using Julia's package manager **Pkg** which will help with things like adding, removing and updating packages, and has its own **REPL** (*read-evaluate-print-loop*). A suggestion before starting and/or creating a new project is to start Julia from the directory that will containg, if not all of them, most of the scripts. So, to enter Pkg REPL just type the right square bracket ```]``` from Julia's REPL. 

Julia's environment created: ```sol_test```