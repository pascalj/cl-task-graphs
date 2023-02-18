# OpenCL Task Graph Extraction

This software is a fork of the [Intercept Layer for OpenCL
Applications](https://github.com/intel/opencl-intercept-layer). Its goal is to solely extract accurate task graphs from
unmodified OpenCL applications during runtime.

This part of the software only implements adequate logging of the relevant data. For further analysis, have a look at
[RESCH](https://github.com/pascalj/resch) that can import he logs and construct and export task graphs from it.

The majority of the original cliloader software is still present, only the necessary adaptions have been made.

An additional dependency is [spdlog](https://github.com/gabime/spdlog) for asynchronous, lock-free logging.

## Usage

Run your application using the `cliloader` binary, e.g. `$ cliloader ./my_code` and after the run, three log files for
timings, events and enqueues are present in the `logs/` directory. For further controls and build instructions, see the
Intercept Layer for OpenCL Applications documentation.

## Status

This software is used for my PhD thesis and implements the subset of functionality that I require. PRs are always
welcome!
