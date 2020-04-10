# gpu-monitoring
ssh instance gpu monitoring on macOS with BitBar

## Installation
1. `brew cask install bitbar`
2. `git clone https://github.com/arnav-gudibande/gpu-monitoring.git`
3. `cd /your/save/path/gpu_monitoring`
4. `chmod +x server_logs.5s.py` 
5. `open -a BitBar` 
6. set bitbar plugin directory to `/your/save/path/gpu_monitoring`
7. bitbar -> preferences -> refresh all

## Configuration

* Adding ssh instances
  - say you want to monitor nvidia-gpu utilization on `example_user_name@example_instance_name`
  - make sure you can ssh to this instance using an ssh key 
  - to add an instance, set `user_name="example_user_name"` and `instance_name="example_instance_name"` in `server_logs.5s.py`
  
* Custom Refresh Rate
  - BitBar refreshes according to the script name, in this case: `server_logs.{timeout}.py`
  - Use BitBar to [set a custom refresh](https://github.com/matryer/bitbar#configure-the-refresh-time)
