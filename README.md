# iwslt2019
IWSLT 2019 dataset with post-editing-based scores and direct assessment annotation.

## IWSLT paper
This dataset was released in the Scarton et al. ["Estimating post-editing effort: a study on human judgements, task-based and reference-based metrics of MT quality"](https://zenodo.org/record/3525003#.Xb0Fti2Q10t) paper. 
```
@proceedings{scarton_scarton_2019_3525003,
  title        = {{Estimating post-editing effort: a study on human 
                   judgements, task-based and reference-based metrics
                   of MT quality}},
  year         = 2019,
  publisher    = {Zenodo},
  month        = nov,
  doi          = {10.5281/zenodo.3525003},
  url          = {https://doi.org/10.5281/zenodo.3525003}
}
```
## Data description
There is a file for each post-editor (ANN0, ANN1, ANN2, ANN3 and ANN4). There is also a file called `header` with a header for each column of the post-editor files. Each file has a segment per line with the following information (separated by a `<tab>` (`\t`) character):

```
file_name: name of the original file
line_in_file: line where this segment appear
who: post-editor	
type: type of the task (this will be PE for all segments)	
src: source id
sys: MT system id
time: PE time	
time/mlen: PE time divide by the machine-translated segment length
slen: source segment length
mlen: machine-translated segment length	
plen: post-edited segment length
schar: number of characters in the source	segment
mchar: number of character in the machine-translated segment
pchar: number of character in the post-edited segment	
letters: letters typed
digits: digits typed
spaces: white chars typed
symbols: special symbols typed
navigation: navigation keystrokes
erase: erasing keystrokes
commands: commands entered (ctrl+c, etc.)
visible: visible keys typed
keystrokes: "total" keystrokes (except commands and navigation)
keystrokes/mchar: keystrokes divide by the number of characters in the machine-translated segments
allkeys: total keystrokes
insertions: PET insertions
deletions: PET deletions
substitutions: PET substitutions
shifts: PET shift
S: source segment	
REF: reference segment	
MT: machine-translated segment	
PE: post-edited segment	
DA: direct assessment score	
HTER: HTER score
HBLEU: HBLEU score	
HMETEOR: HMETEOR score	
TER: TER score
BLEU: BLEU score	
METEOR: METEOR score
