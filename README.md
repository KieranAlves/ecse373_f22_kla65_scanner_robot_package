<h1>This package contains three launch files for running rviz simulations</h1>


<h2>Original launch configuration</h2>
<p>This is the original launch configuration made in lab 2. It opens RVIZ<br>
and shows the robot. Robot has continuous wheel joints.</p>

<h4>ARGUMENTS</h4>
<h6>use_xacro</h6>
<p>This argument controls whether the robot is loaded from either the urdf<br>
or the xacro file. By default it is set to 'false' meaning the urdf file<br>
is run but can be set to 'true' so that the xacro file is run instead.</p>

<h6>use_gui</h6>
<p>This argument controls whether the joint_state_publisher uses it's gui<br>
or not. By default it is set to 'true' meaning that the gui appears, but<br>
it can be set to false so that the gui is not used.</p>

<h4>FILES</h4>
<h6>original.launch</h6>
<p>It is the launch file for this launch configuration and is stored in the<br>
'launch' directory.</p>

<h6>original.rviz</h6>
<p>It is the rviz configuration file for this launch configuration and is<br>
stored in the 'config' directory.</p>

<h6>original.xacro</h6>
<p>It describes the robot in xacro.</p>

<h6>original.urdf</h6>
<p>It describes the robot in urdf. It was made from the original.xacro file.</p>



<h2>Rosbag and sensor configuration</h2>
<p>This is the second launch configuration started at the beginning of<br>
lab 3. It uses the lidar sensors on the robot and takes their simulated<br>
messages from the rosbag to display them in rviz.</p>

<h4>ARGUMENTS</h4>
<h6>ros_bag_location</h6>
<p>As the name suggests, this variable is the location of the ros bag.<br>
If the rosbag is not provided or if the path is incorrect then an error<br>
will be sent but the rest of rviz will work just fine except without dots.</p>

<h6>use_sim_time</h6>
<p>This argument takes either true or false, and if true it will run with<br>
the --clock argument when opening the rosbag. If false it will not.</p>

<h4>FILES</h4>
<h6>basic_laser.launch</h6>
<p>It is the launch file for this launch configuration and is stored in the<br>
'launch' directory. Includes the 'original.xacro' file. It runs the bag file<br>
given the file location.</p>

<h6>basic_laser.rviz</h6>
<p>It is the rviz configuration file for this launch configuration and is<br>
stored in the 'config' directory. Adds elements to the rviz display and<br>
shows all lidar dots for 10 seconds.</p>

<h6>basic_laser.xacro</h6>
<p>It is the file that builds the robot. It adds some new parts but mostly<br>
it will include the original.xacro from the original launch configuration to<br>
build most of the robot.</p>

<h6>versetile_launch.launch</h6>
<p>It is the file from the original launch configuration altered to better<br>
fit this launch configuration. It removes the arguments 'get_gui' and<br>
'use_xacro' because they will not be changed. It also changes which rviz<br>
files are used. </p>




<h2>Glennan map configuration</h2>
<p>This is the third launch configuration finished at the end of lab 3.<br>
It adds the map data and allows the robot to move around the map. It<br>
removes the </p>
<h4>ARGUMENTS</h4>
<h6>ros_bag_location</h6>
<p>This argument takes the location of the rosbag to be used.</p>

<h6>permanent_map</h6>
<p>By default this argument is set to false and the decay time for the<br>
lidar dots is set to 10, but if this argument is set to true then the<br>
decay time for the dots will be set to 1000 and build a very cool map<br>
that will unfortunately probably cause rviz to freeze because too many<br>
dots will be displayed.</p>

<h4>FILES</h4>
<h6>mapping.launch</h6>
<p>This launch configuration really only adds the map file.</p>

<h6>map_scanner.rviz</h6>
<p>It is the same rviz configuration as the last launch configuration<br>
but adds the map to the display and sets the camera to no longer be<br>
following the robot.</p>

<h6>mapping.rviz</h6>
<p>It is the same as map_scanner.rviz but the lidar dots decay is set<br>
to 1000.</p>

<h6>basic_laser.xacro</h6>
<p>It is the file that builds the robot. It adds some new parts but mostly<br>
it will include the original.xacro from the original launch configuration to<br>
build most of the robot.</p>

<h6>versetile_launch.launch</h6>
<p>It is the file from the original launch configuration altered to better<br>
fit this launch configuration. It removes the arguments 'get_gui' and<br>
'use_xacro' because they will not be changed. It also changes which rviz<br>
files are used. </p>
