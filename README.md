# SnPM_test_data
Data for non-regression testing of SnPM

#### To create test data for a new version of Matlab
 1. Clone SnPM test data from https://github.com/SnPM-toolbox/SnPM_test_data. Corresponding folder is denoted by `<SNPM_TEST_DATA_PATH>` in the following.
 1. Clone SnPM from https://github.com/nicholst/SnPM-devel. Corresponding folder is denoted by `<SNPM_PATH>` in the following.
 2. Checkout SnPM8

    ```
    $ cd <SNPM_PATH>
    $ git checkout SnPM8 
    ```
 3. In MATLAB, add the path to SPM and SnPM (not done automatically for SnPM8)

    ```
    >> addpath('<SPM_PATH>')
    >> addpath('<SNPM_PATH>')
    >> addpath('<SNPM_PATH>/test/')
    ```
 4. In `snpm_test_config.m` set the `testDataDir` variable to the path to your SnPM test data folder

    ```
    testDataDir = '<SNPM_TEST_DATA_PATH>'; % Specify directory containing test data
    ```
 4. In MATLAB, run

    ```
    snpm_test_ground_truth
    ```
 6. A window "check SnPM version" opens and says "Current version of SnPM: SnPM8. Is that okay?", answer "yes".
 7. Follow instructions in the MATLAB prompt to create the ground truth data, click "continue" and "done" when prompted.
 8. Once tests have finished, make a copy of the `onesample_1` folder and rename it `onesample_no_ext_in_results` and submit all test-generated results folders and files to GitHub.
