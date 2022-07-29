Quick demo for [BAPL-1963 Incorrect object type returned in a DMN business-rule task of a BPMN](https://issues.redhat.com/browse/BAPL-1963)

Start a BPMN2 which is a straight-through process (STP) with the "name" and "age":

![](/Screenshot_trigger_process_instance.png)

Being an STP we can just "see" the result immediately, here `System.out.println` in the output script of the BPMN2 Task:

![](/Screenshot_java_class_tostring.png)

Notice how the `toString()` from the Java class is hand crafted, to make sure the Java class was used.

Notice the BPMN2 process Data I/O dialogue:

![](/Screenshot_bpmn2_data_io.png)

is specifying the Java class in the output mapping, while the DMN use the classic structural typing (implemented as a `java.util.Map`):

![](/Screenshot_dmn_output.png)
