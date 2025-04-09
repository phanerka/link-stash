*yes, Visual Studio. not Code.*

### Profiling
yeah. 
### Attaching
>[!warning] Won't work with Linux or Ma- hold on how did you install *this thing* THERE?!

Heard of issue of incorrect Visual Studio setup, if the mod is developed there but can't be attached to.
- go to your project properties
- go to build -> general tab, scroll to its bottom
- find "Debug symbols" setting and change it to:
"PDB file, portable across platforms"

and dont forget to rebuild your mod lmao
and move pdb file as well to your mod folder if its not symlinked lmao