---
title: sbatch examples
layout: page
description: how to use sbatch to submit jobs on gizmo
---

# sbatch?

We use the *slurm* scheduler on our HPC cluster _gizmo_. You can use the `sbatch` command to submit a script as a job to the cluster.

## Nodes, tasks, CPUs, and cores... oh, my!

The *slurm* scheduler defines the following terms:
 * tasks `-n <n>` - the number of time to run the job
 * nodes `-N <n>` - the number of different nodes (hosts) to use for the jobs
 * CPUs `-c <n>` - the number of CPU cores to reserve for each task
 * cores == CPUs

## Basic use

To run a script using sbatch, you simply run `sbatch <script>`. To control job execution, you can use command-line parameters from the list above.

Run `ben.sh` on 1 node, 1 time, with 1 core: `sbatch -N 1 -c 1 -n 1 ben.sh`

Most of the time you do not need to use `-N` unless you really need your processes running on either the same machine, or different machines. So we will drop that parameter from examples for clarity.

You would think that to run `ben.sh` four times with one core each, you would use: `sbatch -n 4 -c 1 ben.sh` but you would be wrong. The `sbatch` command is intended to submit a _batch_ of jobs, so the assumption is that the script submitted with `sbatch` actually launches the jobs. When used like this, *slurm* allocates enough core for 4 tasks, but only runs the sbatch script on one of them. In your script, you would then launch more jobs, probably using `srun`.

## Troubleshooting

You can use `squeue -u <username>` to check on your running/pending jobs, and `sacct' to check on no longer running jobs.
