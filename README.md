# ROS_WBMPC

ROS interface for the Whole Body Model Predictive Controller

contents of the packages:
- ros_server_wbmpc_server (optional)
    - eigen interface to ros_server_wbmpc_msgs
    - easier usage of TF (mocap)
    - logger (PAL?)
    - a place to put the crocoddyl code, object usage or inheritance.
- ros_server_wbmpc_client (optional)
    - math to parsing the ros msgs from the server and convert the Ricatti gains into torques ref.
- ros_server_wbmpc_msgs (very practical in terms of ros infrastructure)
    - input msg
    - output msg
- roscontrol_pal_wbmpc (mandatory for safe robot usage!!!!)
    - math of the low level for talos (with parametrization)
        - natively using ros_server_wbmpc_msgs as external interface **OR**
        - using the ros_server_wbmpc_client
    - parametrization of the controlled(torque)/fixed(position) joints.
