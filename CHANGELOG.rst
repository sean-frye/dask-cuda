0.14
----
- Publish branch-0.14 to conda (#262) `Paul Taylor`_
- Fix behavior for `memory_limit=0` (#269) `Peter Andreas Entschev`_
- Raise serialization errors when spilling (#272) `John Kirkham`_
- Fix dask-cuda-worker memory_limit (#279) `Peter Andreas Entschev`_
- Add NVTX annotations for spilling (#282) `Peter Andreas Entschev`_
- Skip existing on conda uploads (#284) `Ray Douglass`_
- Local gpuCI build script (#285) `Eli Fajardo`_
- Remove deprecated DGX class (#286) `Peter Andreas Entschev`_
- Add RDMACM support (#287) `Peter Andreas Entschev`_
- Read the Docs Setup (#290) `Benjamin Zaitlen`_
- Raise ValueError when ucx_net_devices="auto" and IB is disabled (#291) `Peter Andreas Entschev`_
- Multi-node benchmarks (#293) `Peter Andreas Entschev`_
- Add docs for UCX (#294) `Peter Andreas Entschev`_
- Add `--runs` argument to CuPy benchmark (#295) `Peter Andreas Entschev`_
- Fixing LocalCUDACluster example. Adding README links to docs (#297) `Randy Gelhausen`_
- Add `nfinal` argument to shuffle_group, required in Dask >= 2.17 (#299) `Peter Andreas Entschev`_
- Initialize parent process' UCX configuration (#301) `Peter Andreas Entschev`_
- Add Read the Docs link (#302) `John Kirkham`_

0.13
----
- Use RMM's `DeviceBuffer` directly (#235) `John Kirkham`_
- Add RMM pool support from dask-cuda-worker/LocalCUDACluster (#236) `Peter Andreas Entschev`_
- Restrict CuPy to <7.2 (#239) `Benjamin Zaitlen`_
- Fix UCX configurations (#246) `Peter Andreas Entschev`_
- Respect `temporary-directory` config for spilling (#247) `John Kirkham`_
- Relax CuPy pin (#248) `John Kirkham`_
- Added `ignore_index` argument to `partition_by_hash()` (#253) `Mads R. B. Kristensen`_
- Use `"dask"` serialization to move to/from host (#256) `John Kirkham`_
- Drop Numba `DeviceNDArray` code for `sizeof` (#257) `John Kirkham`_
- Support spilling of device objects in dictionaries (#260) `Mads R. B. Kristensen`_

0.12
----

- Add ucx-py dependency to CI (#212) `Ray Douglass`_
- Follow-up revision of local_cudf_merge benchmark (#213) `Richard (Rick) Zamora`_
- Add codeowners file (#217) `Ray Douglass`_
- Add pypi upload script (#218) `Ray Douglass`_
- Skip existing on PyPi uploads (#219) `Ray Douglass`_
- Make benchmarks use rmm_cupy_allocator (#220) `Mads R. B. Kristensen`_
- cudf-merge-benchmark now reports throughput (#222) `Mads R. B. Kristensen`_
- Fix dask-cuda-worker --interface/--net-devices docs (#223) `Peter Andreas Entschev`_
- Use RMM for serialization when available (#227) `Peter Andreas Entschev`_

0.11
----

- Use UCX-Py initialization API (#152) `Peter Andreas Entschev`_
- Remove all CUDA labels (#160) `Mike Wendt`_
- Setting UCX options through dask global config (#168) `Mads R. B. Kristensen`_
- Make test_cudf_device_spill xfail (#170) `Peter Andreas Entschev`_
- Updated CI, cleanup tests and reformat Python files (#171) `Mads R. B. Kristensen`_
- Fix GPU dependency versions (#173) `Dillon Cullinan`_
- Set LocalCUDACluster n_workers equal to the length of CUDA_VISIBLE_DEVICES (#174) `Matthew Rocklin`_
- Simplify dask-cuda code (#175) `Mads R. B. Kristensen`_
- DGX inherit from LocalCUDACluster (#177) `Mads R. B. Kristensen`_
- Single-node CUDA benchmarks (#179) `Mads R. B. Kristensen`_
- Set TCP for UCX tests (#180) `Peter Andreas Entschev`_
- Single-node cuDF merge benchmarks (#183) `Mads R. B. Kristensen`_
- Add black and isort checks in CI (#185) `Peter Andreas Entschev`_
- Remove outdated xfail/importorskip test entries (#188) `Peter Andreas Entschev`_
- Use UCX-Py's TopologicalDistance to determine IB interfaces in DGX (#189) `Peter Andreas Entschev`_
- Dask Performance Report (#192) `Mads R. B. Kristensen`_
- Allow test_cupy_device_spill to xfail (#195) `Peter Andreas Entschev`_
- Use ucx-py from rapidsai-nightly in CI (#196) `Peter Andreas Entschev`_
- LocalCUDACluster sets closest network device (#200) `Mads R. B. Kristensen`_
- Expand cudf-merge benchmark (#201) `Richard (Rick) Zamora`_
- Added --runs to merge benchmark (#202) `Mads R. B. Kristensen`_
- Move UCX code to LocalCUDACluster and deprecate DGX (#205) `Peter Andreas Entschev`_
- Add markdown output option to cuDF merge benchmark (#208) `Benjamin Zaitlen`_

0.10
----

- Change the updated new_worker_spec API for upstream (#128) `Matthew Rocklin`_
- Update TOTAL_MEMORY to match new distributed MEMORY_LIMIT (#131) `Peter Andreas Entschev`_
- Bum Dask requirement to 2.4 (#133) `Matthew Rocklin`_
- Use YYMMDD tag in nightly build (#134) `Markku Luukkainen`_
- Automatically determine CPU affinity (#138) `Peter Andreas Entschev`_
- Fix full memory use check testcase (#139) `Sangeeth Keeriyadath`_
- Use pynvml to get memory info without creating CUDA context (#140) `Peter Andreas Entschev`_
- Pass missing local_directory to Nanny from dask-cuda-worker (#141) `Peter Andreas Entschev`_
- New worker_spec function for worker recipes (#147) `Peter Andreas Entschev`_
- Add new Scheduler class supporting environment variables (#149) `Peter Andreas Entschev`_
- Support for TCP over UCX (#152) `Peter Andreas Entschev`_


.. _`Matthew Rocklin`: https://github.com/mrocklin
.. _`Peter Andreas Entschev`: https://github.com/pentschev
.. _`Markku Luukkainen`: https://github.com/mluukkainen
.. _`Sangeeth Keeriyadath`: https://github.com/ksangeek

0.9
---

- Fix serialization of collections and bump dask to 2.3.0 (#118) `Peter Andreas Entschev`_
- Add versioneer (#88) `Matthieu Bulte`_
- Python CodeCov Integration (#91) `Dillon Cullinan`_
- Update cudf, dask, dask-cudf, distributed version requirements (#97) `Peter Andreas Entschev`_
- Improve device memory spilling performance (#98) `Peter Andreas Entschev`_
- Update dask-cuda for dask 2.2 (#101) `Matthew Rocklin`_
- Streamline CUDA_REL environment variable (#102) `Olli Koskinen`_
- Replace ncores= parameter with nthreads= (#101) `Matthew Rocklin`_
- Fix remove CodeCov upload from build script (#115) `Dillon Cullinan`_
- Remove CodeCov upload (#116) `Dillon Cullinan`_

.. _`Matthieu Bulte`: https://github.com/matthieubulte
.. _`Dillon Cullinan`: https://github.com/dillon-cullinan
.. _`Peter Andreas Entschev`: https://github.com/pentschev
.. _`Matthew Rocklin`: https://github.com/mrocklin
.. _`Olli Koskinen`: https://github.com/okoskinen

0.8
---

-  Add device memory spill support (LRU-based only) (#51) `Peter Andreas Entschev`_
-  Update CI dependency to CuPy 6.0.0 (#53) `Peter Andreas Entschev`_
-  Add a hard-coded DGX configuration (#46) (#70) `Matthew Rocklin`_
-  Fix LocalCUDACluster data spilling and its test (#67) `Peter Andreas Entschev`_
-  Add test skipping functionality to build.sh (#71) `Dillon Cullinan`_
-  Replace use of ncores= keywords with nthreads= (#75) `Matthew Rocklin`_
-  Fix device memory spilling with cuDF (#65) `Peter Andreas Entschev`_
-  LocalCUDACluster calls _correct_state() to ensure workers started (#78) `Peter Andreas Entschev`_
-  Delay some of spilling test assertions (#80) `Peter Andreas Entschev`_


.. _`Peter Andreas Entschev`: https://github.com/pentschev
.. _`Matthew Rocklin`: https://github.com/mrocklin
.. _`Dillon Cullinan`: https://github.com/dillon-cullinan
.. _`Matthieu Bulte`: https://github.com/matthieubulte
.. _`Olli Koskinen`: https://github.com/okoskinen
.. _`John Kirkham`: https://github.com/jakirkham
.. _`Markku Luukkainen`: https://github.com/mluukkainen
.. _`Sangeeth Keeriyadath`: https://github.com/ksangeek
.. _`Mike Wendt`: https://github.com/mike-wendt
.. _`Mads R. B. Kristensen`: https://github.com/madsbk
.. _`Richard (Rick) Zamora`: https://github.com/rjzamora
.. _`Benjamin Zaitlen`: https://github.com/quasiben
.. _`Ray Douglass`: https://github.com/raydouglass
.. _`Paul Taylor`: https://github.com/trxcllnt
.. _`Eli Fajardo`: https://github.com/efajardo-nv
.. _`Randy Gelhausen`: https://github.com/randerzander
