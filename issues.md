# Lab 5: Static Code Analysis — Issues Report

| Issue | Type | Description | Fix implemented |
|---|---|---|---|
| Mutable default argument | Bug | A shared default list could cause guest data to be shared between function calls. | Used `None` and initialized a separate list for each event. |
| Inconsistent naming | Code quality | Function names and parameters did not follow snake_case. | Renamed functions and parameters to follow Python naming conventions. |
| Missing docstrings | Code quality | Functions and the module lacked documentation. | Added module and function docstrings. |
| Unused sorting parameter | Code quality | The guest-report function accepted a sorting parameter without using it. | Implemented ascending and descending guest sorting. |
| Missing event validation | Bug | Looking up a nonexistent event could cause a KeyError. | Added validation and clear error handling. |
| Unsafe pickle loading | Security | Deserializing an untrusted pickle file can execute arbitrary code. | Replaced pickle persistence with JSON and validated loaded data. |
| Unsafe shell command | Security | Using `os.system()` with constructed command strings can create command-injection risks. | Used subprocess with an argument list, `shell=False`, and event-name validation. |
| Missing input validation | Reliability | Invalid capacities, event names, or guest data could cause unexpected behaviour. | Added input validation. |
| Inconsistent formatting | Style | Spacing and formatting were inconsistent. | Improved formatting and used consistent Python style. |

## Summary

Pylint, Bandit and Flake8 were used to analyse the event management program. The issues were reviewed and the code was updated to improve correctness, security, readability and maintainability. The tools were run again to verify the changes.
