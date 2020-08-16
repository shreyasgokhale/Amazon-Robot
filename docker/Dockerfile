FROM rosplanning/navigation2:main.release

COPY . /opt/warehouse_ws/src/

WORKDIR /opt/warehouse_ws/

RUN /bin/bash -c "source /opt/overlay_ws/install/setup.sh && cd /opt/warehouse_ws/ && colcon build --symlink-install"

COPY docker/ros_entrypoint.sh /

RUN chmod 755 /ros_entrypoint.sh

ENTRYPOINT ["/ros_entrypoint.sh"]
CMD ["bash"]


