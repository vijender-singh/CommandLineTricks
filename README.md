```{bash}
screen -dmS qualimap; screen -S qualimap -p 0 -X stuff " srun --pty -p general --qos=general --mem=5G bash -c 'module load qualimap/2.2.1; qualimap rnaseq -bam 3-83522-3_dup_removed_sort.bam -gtf /isg/shared/databases/alignerIndex/animal/mus_musculus/97/Mus_musculus.GRCm38.97.gtf -outdir /labs/Singh/guzzo/qualimap/3-83522-3 --java-mem-size=5G'^M"
```
#### `screen -dmS qualimap`
This will start a new creen session in a dettached mode.

#### `screen -S qualimap -p 0 -X stuff " srun --pty -p general --qos=general --mem=5G bash -c 'module load qualimap/2.2.1; qualimap rnaseq -bam 3-83522-3_dup_removed_sort.bam -gtf /isg/shared/databases/alignerIndex/animal/mus_musculus/97/Mus_musculus.GRCm38.97.gtf -outdir /labs/Singh/guzzo/qualimap/3-83522-3 --java-mem-size=5G'^M"`
This pushes the command `" srun --pty -p general --qos=general --mem=5G bash -c 'module load qualimap/2.2.1; qualimap rnaseq -bam 3-83522-3_dup_removed_sort.bam -gtf /isg/shared/databases/alignerIndex/animal/mus_musculus/97/Mus_musculus.GRCm38.97.gtf -outdir /labs/Singh/guzzo/qualimap/3-83522-3 --java-mem-size=5G'^M"` in the dettached screen.
#### `^M`
This mimics pressing `ENTER` after the command to start executing it.
#### `srun --pty -p general --qos=general --mem=5G bash`
This starts the interactive session in screen.
#### `-c 'module load qualimap/2.2.1; qualimap rnaseq -bam 3-83522-3_dup_removed_sort.bam -gtf /isg/shared/databases/alignerIndex/animal/mus_musculus/97/Mus_musculus.GRCm38.97.gtf -outdir /labs/Singh/guzzo/qualimap/3-83522-3 --java-mem-size=5G'`
This pushes the command in the interactive session.
