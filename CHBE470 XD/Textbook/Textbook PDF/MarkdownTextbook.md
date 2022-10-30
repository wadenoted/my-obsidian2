# MarlinText
## Preamble
### Cover
### Title Page
### About the Author
Thomas E. Marlin is a professor of Chemical Engineering at McMaster University in Hamilton, Ontario, Canada, where he held the NSERC Industrial Research Chair in Process Control. He received his Ph.D. from the University of Massachusetts in 1972. Then, he worked in industry for 15 years where he applied simulation and control to a wide range of continuous process in the chemical and petroleum industries. In 1987, he served as the Visiting Fellow in Sydney, Australia. for the Warren Centre Study on benefits from process control. A team of 40 engineers investigated 7 case studies while refining methods for quantifying benefits from automation. Dr. Marlin is currently Director of the McMaster Advanced Control Consortium, which is a collaboration between university researchers and numerous companies, resulting in leading research that is focused on challenges of great relevance to industrial practitioners. He teaches university courses in process control, process analysis, problem solving, and process design. In addition, he presents industrial short courses on process control, benefits estimation, and optimization. Dr. Marlin's research interests include real-time optimization and process control design.
### Preface
Automation via feedback is not new. Early application of automatic control principles appeared in antiquity, and widespread use of automation began in the nineteenth century when machinery was becoming the dominant method for manufacturing goods. Great advances have been made in theory and practice so that automation is now used in systems as commonplace as room heating and as exciting as the navigation of interplanetary exploration and telecommunications. The great change over the recent years is the integral - at times essential - role of automation in our daily lives and industrial systems. Process control is a subdiscipline of automatic control that involves tailoring methods for the efficient operation of chemical processes. Proper application of process control can improve the safety and profitability of a process, while maintaining consistently high product quality. The automation of selected functions has relieved plant personal of tedious, routine tasks, providing them with time and data to monitor and supervise operations. Essentially every chemical engineer designing or operating plants is involved with and requires a background in process control. This book provides an introduction to process control with emphasis on topics that are of use to the general chemical engineer as well as the specialist. 
### Brief Contents
### Contents
### Symbols and Acronyms
Process control uses many symbols in equations and drawings. The equation symbols are presented here. and the drawing symbols are presented along with common process sketches in Appendix A. The symbols selected for this Table are used multiple times in the book and explained only where they are first used. If a symbol is used only once and explained where used, it is not included in this table. Each entry gives a short description and where appropriate, a reference is given to enable the reader to quickly find further explanation of the symbol and related technology. 
### Quick Reference Guide

#### Mathematical Methods
| Mathematical Methods   | pg  |
| ---------------------- | --- |
| Degree of Freedom      | 55  |
| Frequency distribution | 30  |

## Part 1: Introduction
There is an old adage, " If you do not know where you arc going, any path will do," In other words, a good knowledge o f the goal is essential before one addresses the detail s of a task. Engineers should keep this adage in mind when studying a new, complex topic, because they can easily become 100 involved in the detail s and lose track of the purpose of learning the topic. Process control is introduced in this first. brief part of the book so that the reader will understand the overall goal of process automation and appreciate the need for the technical rigor of the subsequent parts.
The study of process control introduces a new perspective to the mastery of process systems: dynamic operation. Prior engineering courses in the typical curriculum concentrate on steady-slate process behavior, which simplifies early study of processes and provides a basis for establishing proper equipment sizes and determining the best constant operating conditions. However, no process operates at a steady state (with all time derivatives exactly zero), because essentially all external variables, such as feed composition or cooling medium temperature, change. Thus, the process design must consider systems that respond to external disturbances and maintain the process operation in a safe region that yields high-quality products in a profitable manner. The emphasis on good operation, achieved through proper plant design and automation, requires a thorough knowledge of the dynamic operation, which is introduced in this part and covered thoroughly in Part II.
In addition, the study of process control introduces a major new concept: feed-back control. This concept is central to most automation systems that monitor a process and adjust some variables to maintain the system at (or near) desired conditions. Feedback is one of the topics studied and employed by engineers of most subdisciplines, and chemical engineers apply these principles to heat exchangers, mass transfer equipment, chemical reactors, and so forth. Feedback control is introduced in this part and covered in detail in Part Ill. 
Finally, the coverage of these topics in this part is qualitative, because it precedes the introduction of mathematical tools. This qualitative presentation is not a shortcoming; rather, the direct and uncomplicated presentation provides a clear and concise discussion of some central ideas in the book. The reader is advised to return to Part I to clarify the goals before beginning each new part of the book. 
### Chapter 1: Introduction to Process Control
#### 1.1 Introduction 
When observing a chemical process in a plant or laboratory, onc sees flows surging from vessel to vessel, liquids bubbling and boiling, viscous material being extruded. and all key measurements changing continuously, sometimes with small fluctuations and other times in response to major changes. The conclusion immediately drawn is that the world is dynamic! This simple and obvious statement provides the key reason for process control. Only with an understanding of transient behavior of physical systems can engineers design processes that perform well in the dynamic world. In their early training, engineering students learn a great deal about steady-state physical systems, which is natural, because steady-state systems are somewhat easier to understand and provide appropriate learning examples. However, the practicing engineer should have a mastery of dynamic physical systems as well. This book provides the basic information and engineering methods needed to analyze and design plants that function well in a dynamic world. 
Control engineering is an engineering science that is used in many engineering disciplines -for example. chemical, electrical, and mechanical engineering- and it is applied to a wide range of physical systems from electrical circuits to guided missiles to robots. The field of process control encompasses the basic principles most useful when applied to the physicochemical systems often encountered by chemical engineers, such as chemical reactors, heat exchangers, and mass transfer equipment. 
Since the principles covered in this book are basic to most tasks performed by chemical engineers. control engineering is not a narrow specialty but an essential topic for all chemical engineers. For example. plant designers must consider the dynamic operation of all equipment, because the plant will never operate at steady slate (with time derivatives exactly equal to zero). Engineers charged with operating plants must ensure that the proper response is made to the ever-occurring disturbances so that operation is safe and profitable. Finally, engineers performing experiments must control their equipment to obtain the conditions prescribed by their experimental designs. In summary, the task of engineers is to design, construct, and operate a physical system to behave in a desired manner, and an essential element of this activity is sustained maintenance of the system .It the desired conditions-which is process control engineering. 
As you might expect, process control engineering involves a vast body of material, including mathematical analysis and engineering practice. However, before we can begin learning the specific principles and calculations, we must understand the goals of process control and how it complements other aspects of chemical engineering. This chapter introduces these issues by addressing the following questions: 
- What does a control system do? 
- Why is control necessary? 
- Why is control possible? 
- How is control done? 
- Where is control implemented? 
- What does control engineering "engineer"? 
- How is process control documented? 
- What are some sample control strategies? 
#### 1.2 What Does a Control System Do? 
First, we will discuss two examples of control systems encountered in everyday life. Then, we will discuss the features of these systems that are common to most control systems and are generalized in deﬁnitions of the terms control and feedback control.
The ﬁrst example of a control system is a person driving an automobile, as shown in Figure 1.1. The driver must have a goal or objective; normally, this would be to stay in a speciﬁc lane. First, the driver must determine the location of the automobile, which she does by using her eyes to see the position of the automobile on the road. Then, the driver must determine or calculate the change required to maintain the automobile at its desired position on the road. Finally, the driver must change the position of the steering wheel by the amount calculated to bring about the necessary correction. By continuously performing these three functions, the driver can maintain the automobile very close to its desired position as disturbances like bumps and curves in the road are encountered.
The second example is the simple heating system shown in Figure 1.2. The house, in a cold climate, can be maintained near a desired temperature by circulating hot water through a heat exchanger. The temperature in the room is determined by a thermostat, which compares the measured value of the room temperature to a desired range, say 18 to 22°C. If the temperature is below 18°C, the furnace and pump are turned on, and if the temperature is above 22°C, the furnace and pump are turned off. If the temperature is between 18 and 22°C, the furnace and pump statuses remain unchanged. A typical temperature history in a house in given in Figure 1.3, which shows how the temperature slowly drifts between the upper and lower limits. It also exceeds the limits, because the furnace and heat exchanger cannot respond immediately. This approach is termed "on/off" control and can be used when precise control at the desired value is not required. We will cover better control methods, which can maintain important variables much closer to their desired values, later in this book.
Now that we have brieﬂy analyzed two control systems, we shall identify some common features. The ﬁrst is that each uses a speciﬁc value (or range) as a desired value for the controlled variable. When we cover control calculations in Part HI, we will use the term set point for the desired value. Second, the conditions of the system are measured; that is, all control systems use sensors to measure the physical variables that are to be maintained near their desired values. Third, each system has a control calculation, or algorithm, which uses the measured and the desired values to determine a correction to the process operation. The control calculation for the room heater is very simple (on/off), whereas the calculation used by the driver may be very complex. Finally, the results of the calculation are implemented by adjusting some item of equipment in the system, which is termed the ﬁnal control element, such as the steering wheel or the furnace and pump switches. These key features are shown schematically in Figure 1.4, which can be used to represent many control systems.
Now that we have discussed some common control systems and identiﬁed key features, we shall deﬁne the term control. The dictionary provides the deﬁnition for the verb control as "to exercise directing inﬂuence." We will use a similar deﬁnition that is adapted to our purposes. The following deﬁnition suits the two physical examples and the schematic representation in Figure 1.4.

> [!NOTE] Title
> Contents

> [!def]+ control:
> to maintain desired conditions in a physical system by adjusting
selected variables in the system

The control examples have an additional feature that is extremely important. This is feedback, which is deﬁned as follows:

> [!def] feedback control: 
> makes use of an output of a system to inﬂuence an input to the
same system.

For example, the temperature of the room is used, through the thermostat on/off decision, to inﬂuence the hot water ﬂow to the exchanger. When feedback is employed to reduce the magnitude of the difference between the actual and desired values, it is termed "negative feedback." Unless stated otherwise, we will always be discussing negative feedback and will not use the modiﬁer negative. In the social sciences and general vernacular, the phrase "negative feedback" indicates an undesirable change, because most people do not enjoy receiving a signal that tells them to correct an error. Most people would rather receive "positive feedback," a signal telling them to continue a tendency to approach the desired condition. This difference in terminology is unfortunate; we will use the terminology for automatic control, with "negative" indicating a change that tends to approach the desired value, throughout this book without exception.
The importance of feedback in control systems can be seen by considering the alternative without feedback. For example, an alternative approach for achieving the desired room temperature would set the hot water ﬂow based on the measured outside temperature and a model of the heat loss of the house. (This type of predictive approach, termed feedforward, will be encountered later in the book, where its use in combination with feedback will be explained.) The strategy without feedback would not maintain the room near the desired value if the model had errors —as it always would. Some causes of model error might be changes in external wind velocity and direction or inﬂows of air through open windows. On the other hand, feedback control can continually manipulate the ﬁnal element to achieve the de sired value. Thus, feedback provides the powerful feature of enabling a control system to maintain the measured value near its desired value without requiring an exact plant model.
Before we complete this section, the terms input and output are clariﬁed. When used in discussing control systems, they do not necessarily refer to material moving into and out of the system. Here, the term input refers to a variable that causes an output. In the steering example, the input is the steering wheel position, and the output is the position of the automobile. In the room heating example, the input is the fuel to the furnace, and the output is the room temperature. It is essential to recognize that the input causes the output and that this relationship cannot be inverted. The causal relationship inherent in the physical process forces us to select the input as the manipulated variable and the output as the measured variable. Numerous examples with selections of controlled and manipulated variables are presented in subsequent chapters.
Therefore, the answer to the ﬁrst question about the function of control is, "A feedback control system maintains speciﬁc variables near their desired values by applying the four basic features shown in Figure 1.4." Understanding and designing feedback control systems is a major emphasis of this book.
#### 1.3 Why Is Control Necessary? 
A natural second question involves the need for control. There are two major reasons for control, which are discussed with respect to the simple stirred-tank heat exchanger shown in Figure 1.5. The process ﬂuid ﬂows into the tank from a pipe and ﬂows out of the tank by overﬂow. Thus, the volume of the tank is constant. The heating ﬂuid ﬂow can be changed by adjusting the opening of the valve in the heating medium line. The temperature in the tank is to be controlled.

The ﬁrst reason for control is to maintain the temperature at its desired value when disturbances occur. Some typical disturbances for this process occur in the following variables: inlet process ﬂuid ﬂow rate and temperature, heating ﬂuid temperature, and pressure of the heating ﬂuid upstream of the valve. As an exercise, you should determine how the valve should be adjusted (opened or closed) in response to an increase in each of these disturbance variables.

The second reason for control is to respond to changes in the desired value. For example, if the desired temperature in the stirred-tank heat exchanger is increased, the heating valve percent opening would be increased. The desired values are based on a thorough analysis of the plant operation and objectives. This analysis is discussed in Chapter 2, where the main issues are arranged in seven categories:

1. Safety
2. Environmental protection
3. Equipment protection
4. Smooth plant operation and production rate
5. Product quality
6. Proﬁt optimization
7. Monitoring and diagnosis

These issues are translated to values of variables—temperatures, pressures, flows,
and so forth—which are to be controlled.

#### 1.4 Why Is Control Possible? 
The proper design of plant equipment is essential for control to be possible and for control to provide good dynamic performance. Therefore, the control and dynamic operation is an important factor in plant design. Based on the key features of feedback control shown in Figure 1.4, the plant design must include adequate sensors of plant output variables and appropriate ﬁnal control elements. The sensors must respond rapidly so that the control action can be taken in real time. Sensors using various physical principles are available for the basic process variables (ﬂow, temperature, pressure, and level), compositions (e.g., mole fraction) and physical properties (e.g., density, viscosity, heat of combustion). Many of these sensors are inserted into the process equipment, with a shield protecting them from corrosive effects of the streams. Others require a sample to be taken periodically from the process; note that this sampling can be automated so that a new sensor result is available at frequent intervals. The ﬁnal control elements in chemical processes are usually valves that affect ﬂuid ﬂows, but they could be other manipulated variables, such as power to an electric motor or speed of a conveyor belt.

Another important consideration is the capacity of the process equipment. The equipment must have a large enough maximum capacity to respond to all expected disturbances and changes in desired values. For the stirred-tank heat exchanger, the maximum duty, as inﬂuenced by temperature, area, and heating medium ﬂow rate, must be large enough to maintain the tank temperature for all anticipated disturbances. This highest heat duty corresponds to the the highest outlet temperature, the highest process ﬂuid ﬂow, the lowest inlet ﬂuid temperature, and the highest heat loss to the environment. Each process must be analyzed to ensure that adequate capacity exists. Further discussion of this topic appears in the next two chapters.

Therefore, the answer to why control is possible is that we anticipate the expected changes in plant variables and provide adequate equipment when the plant is designed. The adequate equipment design for control must be calculated based on expected changes; merely adding extra capacity, say 20 percent, to equipment sizing is not correct. In some cases, this would result in waste; in other cases, the equipment capacity would not be adequate. If this analysis is not done properly or changes outside the assumptions occur, achieving acceptable plant operation through manipulating ﬁnal control elements may not be possible.

#### 1.5 How Is Control Done? 
As we have seen in the automobile driving example, feedback control by human actions is possible. In some cases, this approach is appropriate, but the continuous, repetitious actions are tedious for a person. In addition, some control calculations are too complex or must be implemented too rapidly to be performed by a person. Therefore, most feedback control is automated, which requires that the key functions of sensing, calculating, and manipulating be performed by equipment and that each element communicate with other elements in the control system. Currently, most automatic control is implemented using electronic equipment, which uses levels of current or voltage to represent values to be communicated. As would be expected, many of the computing and some of the communication functions are being performed increasingly often with digital technology. In some cases control systems use pneumatic, hydraulic, or mechanical mechanisms to calculate and communicate; in these systems, the signals are represented by pressure or physical position. A typical process plant will have examples of each type of instrumentation and communication.

Since an essential aspect of process control is instrumentation, this book intro duces some common sensors and valves, but proper selection of this equipment for plant design requires reference to one of the handbooks in this area for additional details. Readers are encouraged to be aware of and use the general references listed at the end of this chapter.

Obviously, the other key element of process control is a device to perform the calculations. For much of the history of process plants (up to the 1960s), control calculations were performed by analog computation. Analog computing devices are implemented by building a physical system, such as an electrical circuit or mechanical system, that obeys the same equations as the desired control calculation. As you can imagine, this calculation approach was inﬂexible. In addition, complex calculations were not possible. However, some feedback control is still implemented in this manner, for reasons of cost and reliability in demanding plant conditions.

With the advent of low-cost digital computers, most of the control calculations and essentially all of the complex calculations are being performed by digital computers. Most of the principles presented in this book can be implemented in either analog or digital devices. When covering basic principles in this book, we will not distinguish between analog and digital computing unless necessary, because the distinction between analog and digital is not usually important as long as the digital computer can perform its discrete calculations quickly. Special aspects of digital control are introduced in Chapter 11. In all chapters after Chapter 11, the control principles are presented along with special aspects of either analog or digital implementation; thus, both modes of performing calculations are covered in an integrated manner.

For the purposes of this book, the answer to the question "How is control done?" is simply, "Automatically, using instrumentation and computation that perform all features of feedback control without requiring (but allowing) human intervention."
#### 1.6 Where Is Control Implemented? 
Chemical plants are physically large and complex. The people responsible for operating the plant on a minute-to-minute basis must have information from much of the plant available to them at a central location. The most common arrangement of control equipment to accommodate this need is shown in Figure 1.6. Naturally, the sensors and valves are located in the process. Signals, usually electronic, communicate with the control room, where all information is displayed to the operating personnel and where control calculations are performed. Distances between the process and central control room range from a few hundred feet to a mile or more. Some control is performed many miles from the process; for example, a remote oil well can have no human present and would rely on remote automation for proper operation.

In the control room, an individual is responsible for monitoring and operating a section of a large, complex plant, containing up to 100 controlled variables and 400 other measured variables. Generally, the plant never operates on "automatic pilot"; a person is always present to perform tasks not automated, to optimize operations, and to intervene in case an unusual or dangerous situation occurs, such as an equipment failure. Naturally, other people are present at the process equipment, usually referred to as "in the ﬁeld," to monitor the equipment and to perform functions requiring manual intervention, such as backwashing ﬁlters. Thus, well-automated chemical plants involve considerable interaction between people and control calculations.

Other control conﬁgurations are possible and are used when appropriate. For example, small panels with instrumentation can be placed near a critical piece of process equipment when the operator needs to have access to the control system while introducing some process adjustments. This arrangement would not prevent the remainder of the plant from being controlled from a central facility. Also, many sensors provide a visual display of the measured value, which can be seen by the local operator, as well as a signal transmitted to the central control room. Thus, the local operator can determine the operating conditions of a unit, but the individual local displays are distributed about the plant, not collected in a single place for the local operator.
The short answer to the location question is
1. Sensors, local indicators, and valves are in the process.
2. Displays of all plant variables and control calculations are in a centralized facility

It is worth noting that increased use of digital computing makes the distribution of the control calculation to the sensor locations practical; however, all controllers would be connected to a computing network that would function like a single computer for the purposes of the material in this book.

#### 1.7 What Does Control Engineering "Engineer"? 
What can engineers do so that plants can be maintained reliably and safely near desired values? Most of the engineering decisions are introduced in the following ﬁve topics.
##### Process Design
A key factor in engineering is the design of the process so that it can be controlled well. We noted in the room heating example that the temperature exceeded the maximum and minimum values because the furnace and heat exchanger were not able to respond rapidly enough. Thus, a more "responsive" plant would be easier to control. By responsive we mean that the controlled variable responds quickly to adjustments in the manipulated variable. Also, a plant that is susceptible to few disturbances would be easier to control. Reducing the frequency and magnitude of disturbances could be achieved by many means; a simple example is placing a large mixing tank before a unit so that feed composition upsets are attenuated by the averaging effects of the tank. Many more approaches to designing responsive processes with few disturbances are covered in the book.
##### Measurements
Naturally, a key decision is the selection and location of sensors, because one can control only what is measured! The engineer should select sensors that measure important variables rapidly and with sufﬁcient accuracy. In this book, we will concentrate on the process analysis related to variable selection and to determining response time and accuracy needs. Details of a few common sensors are also presented as needed in exercises; a full review of sensor technology and commercial equipment is available in the references at the end of this chapter.
##### Final Elements
The engineer must provide handles—manipulated variables that can be adjusted by the control calculation. For example, if there were no valve on the heating ﬂuid in Figure 1.5, it would not be possible to control the process ﬂuid outlet temperature. This book concentrates on the process analysis related to ﬁnal element location. We will typically be considering control valves as the ﬁnal elements, with the percentage opening of these valves determined by a signal sent to the valve from a controller. Speciﬁc details about the best ﬁnal element to regulate ﬂow of various fluids—liquids, steam, slurries, and so forth—are provided by references noted at the end of this chapter. These references also present other ﬁnal elements, such as motor speed, that are used in the process industries.
##### Control Structure
The engineer must decide some very basic issues in designing a control system. For example, which valve should be manipulated to control which measurement? As an everyday example, one could adjust either the hot or cold water valve opening to control the temperature of water in a shower. These topics are presented in later chapters, after a sound basis of understanding in dynamics and feedback control principles has been built.
##### Control Calculations
After the variables and control structure have been selected, equation(s) are chosen that use the measurement and desired values in calculating the manipulated variable. As we shall learn, only a few equations are sufﬁcient to provide good control for many types of plants. After the control equations' structure is deﬁned, parameters that appear in the equations are adjusted to achieve the desired control performance for the particular process.
#### 1.8 How Is Process Control Documented? 
As with all activities in chemical engineering, the results are documented in many forms. The most common are equipment speciﬁcations and sizing, operating manuals, and technical documentation of plant experiments and control equations. In addition, control engineering makes extensive use of drawings that concisely and unequivocally represent many design decisions. These drawings are used for many purposes, including designing plants, purchasing equipment, and reviewing operations and safety procedures. Therefore, many people use them, and to avoid misunderstandings standard symbols have been developed by the Instrument Society of America for use throughout the world. We shall adhere to a reduced version of this excellent standard in this book because of its simplicity and wide application. 

Sample drawings are shown in Figure 1.7. All process equipment—piping, vessels, valves, and so forth—is drawn in solid lines. The symbols for equipment items such as pumps, tanks, drums, and valves are simple and easily recognized. Sensors are designated by a circle or "bubble" connected to the point in the process where they are located. The ﬁrst letter in the instrumentation symbol indicates the type of variable measured; for example, "T" corresponds to temperature. Some of the more common designations are the following:

| symbol | definition                                                                                            |
| ------ | ----------------------------------------------------------------------------------------------------- |
| A      | Analyzer (speciﬁc analysis is often indicated next to the symbol, for example, p (for density) or pH) |
| F      | Flow rate                                                                                             |
| L      | level of liquid or solids in a vessel                                                                 |
| P      | pressure                                                                                              |
| T      | temperature                                                                                           |

Note that the symbol does not indicate the physical principle used by the sensor.
Backup tabular documentation is required to determine such details.

The communication to the sensor is shown as a solid line. If the signal is used only for display to the operator, the second letter in the symbol is "I" for indicator. Often, the "I" is not used, so that a single letter refers to a measurement used for monitoring only, not for control.

If the signal is used in a calculation, it is also shown in a circle. The second letter in the symbol indicates the type of calculation. We consider only two possibilities in this book: "C" for feedback control and "Y" for any other calculation, such as addition or square root. The types of control calculations are covered later in the book. A noncontrol calculation might use the measured ﬂow and temperatures around a heat exchanger to calculate the duty; that is, $Q = \rho C_{p} F \left( T_{m}-T_{out} \right)$. For controllers, the communication to the ﬁnal element is shown as a dashed line when it is electrical, which is the mode communication considered in designs for most of this book.

The basic symbols with their meanings are documented in Appendix A. This simpliﬁed version of the Instrument Society of America standards is sufﬁcient for this textbook and will provide an adequate background for more complex drawings. While using the standards may seem like additional work in the beginning, it should be considered a small investment leading to accurate communication, like learning grammar and vocabulary, used by all chemical engineers.

#### 1.9 What Are Some Sample Control Strategies? 
Some very simple example process control systems are given in Figure 1.7a through d. Each drawing contains a process schematic, a controller (in the instrumentation circle), and the connection between the measurement and the manipulated variable. As a thought exercise, you should analyze each process control system to verify the causal process relationship and to determine what action the controller would take in response to a disturbance or a change in desired value (set point). For example, in Figure 1 .la, with an increase in the inlet temperature, the control system would sense a decrease in the outlet composition of reactant. In response, the control system would adjust the heating coil valve, closing it slightly, until the outlet composition returned to its desired value.

A sample of a more complex process diagram, this one without the control design, is given in Figure 1.8. The process includes a chemical reactor, a ﬂash separator, heat exchangers, and associated piping. Note that a control design engineer must select from a large number of possible measurements and valves to determine controller connections from an enormous number of possibilities! In Chapter 25 you will design a control system for this process that controls the key variables, such as reactor level and separator temperature, based on speciﬁed control objectives.

#### 1.10 Conclusions 
The material in this chapter has presented a qualitative introduction to process control. You have learned the key features of feedback control along with the types of equipment (instruments and computers) required to apply process control. The importance of the process design on control was discussed several times in the chapter.

Based on this introduction, we are prepared to discuss more carefully the goals of process control in Chapter 2. Understanding the process control goals is essential to selecting the type of analysis used in control engineering.
### Chapter 2: Control Objectives and Benefits
#### 2.1 Introduction 
The ﬁrst chapter provided an overview of process control in which the close association between process control and plant operation was noted. As a consequence, control objectives are closely tied to process goals, and control beneﬁts are closely tied to attaining these goals. In this chapter the control objectives and beneﬁts are discussed thoroughly, and several process examples are presented. The control objectives provide the basis for all technology and design methods presented in subsequent chapters of the book.

While this book emphasizes the contribution made by automatic control, con trol is only one of many factors that must be considered in improving process performance. Three of the most important factors are shown in Figure 2.1, which indicates that proper equipment design, operating conditions, and process control should all be achieved simultaneously to attain safe and proﬁtable plant operation. Clearly, equipment should be designed to provide good dynamic responses in addi tion to high steady-state proﬁt and efﬁciency, as covered in process design courses and books. Also, the plant operating conditions, as well as achieving steady-state plant objectives, should provide ﬂexibility for dynamic operation. Thus, achiev ing excellence in plant operation requires consideration of all factors. This book addresses all three factors; it gives guidance on how to design processes and select operating conditions favoring good dynamic performance, and it presents automa tion methods to adjust the manipulated variables.

#### 2.2 Control Objectives 
The seven major categories of control objectives were introduced in Chapter 1. They are discussed in detail here, with an explanation of how each inﬂuences the control design for the example process shown in Figure 2.2. The process separates two components based on their different vapor pressures. The liquid feed stream, consisting of components A and B, is heated by two exchangers in series. Then the stream ﬂows through a valve to a vessel at a lower pressure. As a result of the higher temperature and lower pressure, the material forms two phases, with most of the A in the vapor and most of the B in the liquid. The exact compositions can be determined from an equilibrium ﬂash calculation, which simultaneously solves the material, energy, and equilibrium expressions. Both streams leave the vessel for further processing, the vapor stream through the overhead line and the liquid stream out from the bottom of the vessel. Although a simple process, the heat exchanger with ﬂash drum provides examples of all control objectives, and this process is analyzed quantitatively with control in Chapter 24. A control strategy is also shown in Figure 2.2. Since we have not yet studied the calculations used by feedback controllers, you should interpret the controller as a linkage between a measurement and a valve. Thus, you can think of the feedback pressure control (PC) system as a system that measures the pressure and maintains the pressure close to its desired value by adjusting the opening of the valve in the overhead vapor pipe. The type of control calculation, which will be covered in depth in later chapters, is not critical for the discussions in this chapter.
##### Safety
The safety of people in the plant and in the surrounding community is of paramount importance. While no human activity is without risk, the typical goal is that working at an industrial plant should involve much less risk than any other activity in a person's life. No compromise with sound equipment and control safety practices is acceptable.

Plants are designed to operate safely at expected temperatures and pressures; however, improper operation can lead to equipment failure and release of potentially hazardous materials. Therefore, the process control strategies contribute to the overall plant safety by maintaining key variables near their desired values. Since these control strategies are important, they are automated to ensure rapid and complete implementation. In Figure 2.2, the equipment could operate at high pressures under normal conditions. If the pressure were allowed to increase too far beyond the normal value, the vessel might burst, resulting in injuries or death. Therefore, the control strategy includes a controller labelled "PC-1" that controls the pressure by adjusting the valve position (i.e., percent opening) in the vapor line.

Another consideration in plant safety is the proper response to major incidents, such as equipment failures and excursions of variables outside of their acceptable bounds. Feedback strategies cannot guarantee safe operation; a very large disturbance could lead to an unsafe condition. Therefore, an additional layer of control, termed an emergency system, is applied to enforce bounds on key variables. Typically, this layer involves either safely diverting the ﬂow of material or shutting down the process when unacceptable conditions occur. The control strategies are usually not complicated; for example, an emergency control might stop the feed to a vessel when the liquid level is nearly overﬂowing. Proper design of these emergency systems is based on a structured analysis of hazards (Battelle Labora tory, 1985; Warren Centre, 1986) that relies heavily on experience about expected incidents and on the reliability of process and control equipment.

In Figure 2.2, the pressure is controlled by the element labelled "PC." Normally, it maintains the pressure at or near its desired value. However, the control strategy relies on the proper operation of equipment like the pressure sensor and the valve. Suppose that the sensor stopped providing a reliable measurement; the control strategy could improperly close the overhead valve, leading to an unsafe pressure. The correct control design would include an additional strategy using independent equipment to prevent a very high pressure. For example, the safety valve shown in Figure 2.2 is closed unless the pressure rises above a speciﬁed maximum; then, it opens to vent the excess vapor. It is important to recognize that this safety relief system is called on to act infrequently, perhaps once per year or less often; therefore, its design should include highly reliable components to ensure that it performs properly when needed.

##### Environmental Protection
Protection of the environment is critically important. This objective is mostly a process design issue; that is, the process must have the capacity to convert potentially toxic components to benign material. Again, control can contribute to the proper operation of these units, resulting in consistently low efﬂuent concentrations. In addition, control systems can divert efﬂuent to containment vessels should any extreme disturbance occur. The stored material could be processed at a later time when normal operation has been restored.

In Figure 2.2, the environment is protected by containing the material within the process equipment. Note that the safety release system directs the material for containment and subsequent "neutralization," which could involve recycling to the process or combusting to benign compounds. For example, a release system might divert a gaseous hydrocarbon to a ﬂare for combustion, and it might divert a water- based stream to a holding pond for subsequent puriﬁcation through biological treatment before release to a water system.

##### Equipment Protection
Much of the equipment in a plant is expensive and difﬁcult to replace without costly delays. Therefore, operating conditions must be maintained within bounds to prevent damage. The types of control strategies for equipment protection are similar to those for personnel protection, that is, controls to maintain conditions near desired values and emergency controls to stop operation safely when the process reaches boundary values.

In Figure 2.2, the equipment is protected by maintaining the operating con ditions within the expected temperatures and pressures. In addition, the pump could be damaged if no liquid were ﬂowing through it. Therefore, the liquid level controller, by ensuring a reservoir of liquid in the bottom of the vessel, protects the pump from damage. Additional equipment protection could be provided by adding an emergency controller that would shut off the pump motor when the level decreased below a speciﬁed value.
##### Smooth Operation and Production Rate
A chemical plant includes a complex network of interacting processes; thus, the smooth operation of a process is desirable, because it results in few disturbances to all integrated units. Naturally, key variables in streams leaving the process should be maintained close to their desired values (i.e., with small variation) to prevent disturbances to downstream units. In Figure 2.2, the liquid from the vessel bottoms is processed by downstream equipment. The control strategy can be designed to make slow, smooth changes to the liquid ﬂow. Naturally, the liquid level will not remain constant, but it is not required to be constant; the level must only remain within speciﬁed limits. By the use of this control design, the downstream units would experience fewer disturbances, and the overall plant would perform better.

There are additional ways for upsets to be propagated in an integrated plant. For example, when the control strategy increases the steam ﬂow to heat exchanger E-102, another unit in the plant must respond by generating more steam. Clearly, smooth manipulations of the steam ﬂow require slow adjustments in the boiler operation and better overall plant operation. Therefore, we are interested in both the controlled variables and the manipulated variables. Ideally, we would like to have tight regulation of the controlled variables and slow, smooth adjustment of the manipulated variables. As we will see, this is not usually possible, and some compromise is required.

People who are operating a plant want a simple method for maintaining the production rate at the desired value. We will include the important production rate goal in this control objective. For the ﬂash process in Figure 2.2, the natural method for achieving the desired production rate is to adjust the feed valve located before the ﬂash drum so that the feed ﬂow rate $F_{1}$ has the desired value.

##### Product Quality
The ﬁnal products from the plant must meet demanding quality speciﬁcations set by purchasers. The speciﬁcations may be expressed as compositions (e.g., percent of each component), physical properties (e.g., density), performance properties (e.g., octane number or tensile strength), or a combination of all three. Process control contributes to good plant operation by maintaining the operating condi tions required for excellent product quality. Improving product quality control is a major economic factor in the application of digital computers and advanced control algorithms for automation in the process industries.

In Figure 2.2, the amount of component A, the material with the higher vapor pressure, is to be controlled in the liquid stream. Based on our knowledge of thermodynamics, we know that this value can be controlled by adjusting the ﬂash temperature or, equivalently, the heat exchanged. Therefore, a control strategy would be designed to measure the composition in real time and adjust the heating medium ﬂows that exchange heat with the feed.

##### Proﬁt
Naturally, the typical goal of the plant is to return a proﬁt. In the case of a utility such as water puriﬁcation, in which no income from sales is involved, the equivalent goal is to provide the product at lowest cost. Before achieving the proﬁt-oriented goal, selected independent variables are adjusted to satisfy the ﬁrst ﬁve higher- priority control objectives. Often, some independent operating variables are not speciﬁed after the higher objectives (that is, including product quality but excepting proﬁt) have been satisﬁed. When additional variables (degrees of freedom) exist, the control strategy can increase proﬁt while satisfying all other objectives.

In Figure 2.2 all other control objectives can be satisﬁed by using exchanger E-101, exchanger E-102, or a combination of the two, to heat the inlet stream. Therefore, the control strategy can select the correct exchanger based on the cost of the two heating ﬂuids. For example, if the process ﬂuid used in E-101 were less costly, the control strategy would use the process stream for heating preferentially and use steam only when required for additional heating. How the control strategy would implement this policy, based on a selection hierarchy deﬁned by the engineer, is covered in Chapter 22.

##### Monitoring and Diagnosis
Complex chemical plants require monitoring and diagnosis by people as well as excellent automation. Plant control and computing systems generally provide mon itoring features for two sets of people who perform two different functions: (1) the immediate safety and operation of the plant, usually monitored by plant operators, and (2) the long-term plant performance analysis, monitored by supervisors and engineers.

The plant operators require very rapid information so that they can ensure that the plant conditions remain within acceptable bounds. If undesirable situations occur—or, one hopes, before they occur—the operator is responsible for rapid recognition and intervention to restore acceptable performance. While much of this routine work is automated, the people are present to address complex issues that are difﬁcult to automate, perhaps requiring special information not readily available to the computing system. Since the person may be responsible for a plant section with hundreds of measured variables, excellent displays are required. These are usually in the form of trend plots of several associated variables versus time and of indicators in bar-chart form for easy identiﬁcation of normal and abnormal operation. Examples are shown in Figure 2.3.

Since the person cannot monitor all variables simultaneously, the control sys tem includes an alarm feature, which draws the operator's attention to variables that are near limiting values selected to indicate serious maloperation. For exam ple, a high pressure in the ﬂash separator drum is undesirable and would at the least result in the safety valve opening, which is not desirable, because it diverts material and results in lost proﬁt and because it may not always reclose tightly. Thus, the system in Figure 2.2 has a high-pressure alarm, PAH. If the alarm is ac tivated, the operator might reduce the ﬂows to the heat exchanger or of the feed to reduce pressure. This operator action might cause a violation of product speciﬁca tions; however, maintaining the pressure within safe limits is more important than product quality. Every measured variable in a plant must be analyzed to determine whether an alarm should be associated with it and, if so, the proper value for the alarm limit.

Another group of people monitors the longer-range performance of the plant to identify opportunities for improvement and causes for poor operation. Usually, a substantial sample of data, involving a long time period, is used in this analysis, so that the effects of minor ﬂuctuations are averaged out. Monitoring involves important measured and calculated variables, including equipment performances (e.g., heat transfer coefﬁcients) and process performances (e.g., reactor yields and material balances). In the example ﬂash process, the energy consumption would be monitored. An example trend of some key variables is given in Figure 2.4, which shows that the ratio of expensive to inexpensive heating source had an increasing trend. If the feed ﬂow and composition did not vary signiﬁcantly, one might suspect that the heat transfer coefﬁcient in the ﬁrst heat exchanger, E-101, was decreasing due to fouling. Careful monitoring would identify the problem and enable the engineer to decide when to remove the heat exchanger temporarily for mechanical cleaning to restore a high heat transfer coefﬁcient.

Previously, this monitoring was performed by hand calculations, which was a tedious and inefﬁcient method. Now, the data can be collected, processed if additional calculations are needed, and reported using digital computers. This com bination of ease and reliability has greatly improved the monitoring of chemical process plants.

Note that both types of monitoring—the rapid display and the slower process analysis—require people to make and implement decisions. This is another form of feedback control involving personnel, sometimes referred to as having "a person in the loop," with the "loop" being the feedback control loop. While we will concentrate on the automated feedback system in a plant, we must never forget that many of the important decisions in plant operation that contribute to longer-term safety and proﬁtability are based on monitoring and diagnosis and implemented by people "manually."

Therefore,

> [!NOTE]
> All seven categories of control objectives must be achieved simultaneously; failure to do so leads to unproﬁtable or, worse, dangerous plant operation.

In this section, instances of all seven goals were identiﬁed in the simple heater and ﬂash separator. The analysis of more complex process plants in terms of the goals is a challenging task, enabling engineers to apply all of their chemical engineering skills. Often a team of engineers and operators, each with special experiences and insights, performs this analysis. Again, we see that control engineering skills are needed by all chemical engineers in industrial practice.

#### 2.3 Determining Plant Operating Conditions 
A key factor in good plant operation is the determination of the best operating conditions, which can be maintained within small variation by automatic control strategies. Therefore, setting the control objectives requires a clear understanding of how the plant operating conditions are determined. A complete study of plant objectives requires additional mathematical methods for simulating and optimizing the plant operation. For our purposes, we will restrict our discussion in this section to small systems that can be analyzed graphically.

Determining the best operating conditions can be performed in two steps. First, the region of possible operation is deﬁned. The following are some of the factors that limit the possible operation:
- Physical principles; for example, all concentrations > 0
- Safety, environmental, and equipment protection
- Equipment capacity; for example, maximum flow
- Product quality

The region that satisﬁes all bounds is termed the feasible operating region or, more commonly, the operating window. Any operation within the operating window is possible. Violation of some of the limits, called soft constraints, would lead to poor product quality or reduction of long-term equipment life; therefore, short- term violations of soft constraints are allowed but are to be avoided. Violation of critical bounds, called hard constraints, could lead to injury or major equipment damage; violations of hard constraints are not acceptable under any foreseeable circumstances. The control strategy must take aggressive actions, including shut ting down the plant, to prevent hard constraint violations. For both hard and soft constraints, debits are incurred for violating constraints, so the control system is designed to maintain operation within the operating window. While any operation within the window is possible and satisﬁes minimum plant goals, a great difference in proﬁt can exist depending on the conditions chosen. Thus, the plant economics must be analyzed to determine the best operation within the window. The control strategy should be designed to maintain the plant conditions near their most proﬁtable values.

The example shown in Figure 2.5 demonstrates the operating window for a simple, one-dimensional case. The example involves a ﬁred heater (furnace) with a chemical reaction occurring as the ﬂuid ﬂows through the pipe or, as it is often called, the coil. The temperature of the reactor must be held between minimum (no reaction) and maximum (metal damage or excessive side reactions) temperatures. When economic objectives favor increased conversion of feed, the proﬁt function monotonically increases with increasing temperature; therefore, the best operation would be at the maximum allowable temperature. However, the dynamic data show that the temperature varies about the desired value because of disturbances such as those in fuel composition and pressure. Therefore, the effectiveness of the control strategy in maximizing proﬁt depends on reducing the variation of the temperature. A small variation means that the temperature can be operated very close to, without exceeding, the maximum constraint.

Another example is the system shown in Figure 2.6, where fuel and air are mixed and combusted to provide heat for a boiler. The ratio of fuel to air is important. Too little air (oxygen) means that some of the fuel is uncombusted and wasted, whereas excess air reduces the ﬂame temperature and, thus, the heat transfer. Therefore, the highest efﬁciency and most proﬁtable operation are near the stoichiometric ratio. (Actually, the best value is usually somewhat above the stoichiometric ratio because of imperfect mixing, leakage, and complex combustion chemistry.) The maximum air ﬂow is determined by the air compressor and is usually not a limitation, but a large excess of air leads to extremely high fuel costs. Therefore, the best plant operation is at the peak of the efﬁciency curve. An effective control strategy results in a small variation in the excess oxygen in the ﬂue gas, allowing operation near the peak.

However, a more important factor is safety, which provides another reason for controlling the excess air. A deﬁciency of oxygen could lead to a dangerous condition because of unreacted fuel in the boiler combustion chamber. Should this situation occur, the fuel could mix with other air (that leaks into the furnace chamber) and explode. Therefore, the air ﬂow should never fall below the stoichiometric value. Note that the control sketch in Figure 2.6 is much simpler than actual control designs for combustion systems (for example, API, 1977).

Finally, a third example demonstrates that this analysis can be extended to more than one dimension. We now consider the chemical reactor in Figure 2.5 with two variables: temperature and product ﬂow. The temperature bounds are the same, and the product ﬂow has a maximum limitation because of erosion of the pipe at the exit of the ﬁred heater. The proﬁt function, which would be calculated based on an analysis of the entire plant, is given as contours in the operating window in Figure 2.7. In this example, the maximum proﬁt occurs outside the operating window and therefore cannot be achieved. The best operation inside the window would be at the maximum temperature and ﬂow, which are found at the upper right-hand corner of the operating window. As we know, the plant cannot be operated exactly at this point because of unavoidable disturbances in variables such as feed pressure and fuel composition (which affects heat of combustion). However, good control designs can reduce the variation of temperature and ﬂow so that desired values can be selected that nearly maximize the achievable proﬁt while not violating the constraints. This situation is shown in Figure 2.7, where a circle deﬁnes the variation expected about the desired values (Perkins, 1990; Narraway and Perkins, 1993). When control provides small variation, that is, a circle of small radius, the operation can be maintained closer to the best operation.

All of these examples demonstrate that

> [!note]
> Process control improves plant performance by reducing the variation of key variables. When the variation has been reduced, the desired value of the controlled variable can be adjusted to increase proﬁt.

Note that simply reducing the variation does not always improve plant op eration. The proﬁt contours within the operating window must be analyzed to determine the best operating conditions that take advantage of the reduced varia tion. Also, it is important to recognize that the theoretical maximum proﬁt cannot usually be achieved because of inevitable variation due to disturbances. This situ ation should be included in the economic analysis of all process designs.


#### 2.4 Benefits for Control 
The previous discussion of plant operating conditions provides the basis for calculating the beneﬁts for excellent control performance. In all of the examples discussed qualitatively in the previous section, the economic beneﬁt resulted from reduced variation of key variables. Thus, the calculation of beneﬁts considers the effect of variation on plant proﬁt. Before the method is presented, it is emphasized that the highest-priority control objectives—namely, safety, environmental protection, and equipment protection—are not analyzed by the method described in this section. Although the control designs for these objectives often reduce variation, they are not selected for increasing proﬁt but rather for providing safe, reliable plant operation. 

Once the proﬁt function has been determined, the beneﬁt method needs to characterize the variation of key plant variables. This can be done through the calculation shown schematically in Figure 2.8. The plant operating data, which is usually given as a plot or trend versus time, can be summarized by a frequency distribution. The frequency distribution can be determined by taking many sample measurements of the process variable, usually separated by a constant time period, and counting the number of measurements whose values fall in each of several intervals within the range of data values. The total time period covered must be long compared to the dynamics of the process, so that the effects of time correlation in the variable and varying disturbances will be averaged out.

The resulting distribution is plotted as frequency; that is, as fraction or percent of measurements falling within each interval versus the midpoint value of that interval. Such a plot is called a frequency distribution or histogram. If the variable were constant, perhaps due to perfect control or the presence of no disturbances, the distribution would have one bar, at the constant value, rising to 1.0 (or 100%). As the variation in the values increases, the distribution becomes broader; thus, the frequency distribution provides a valuable summary of the variable variation.

The distribution could be described by its moments; in particular, the mean and standard deviation are often used in describing the behavior of variables in feedback systems (Snedecor and Cochran, 1980; Bethea and Rhinehart, 1991). These values can be calculated from the plant data according to the following equations:
> [!mathz] Eqns 2.1, 2.2
> > [!eqn]+ Eqn (2.1)
> > $$\text{Mean}=\bar{Y}=\frac{1}{n} \sum \limits _{i=1}^{n} Y_{i}$$
> 
> > [!eqn]+ Eqn (2.2)
> > $$\text{Standard deviation} = s_{Y} = \sqrt {\frac {\sum_{i=1} ^n\left( Y_{i} - \bar{Y} \right) ^2} {n-1}}$$
> 
> where 
> $$ \begin{align}
Y_{i} &= \text { measured value of variable } \\
s_Y^2 &= \text { variance } \\
n &= \text { number of data points }
\end{align}$$

When the experimental distribution can be characterized by the standard nor mal distribution, the variation about the mean is characterized by the standard deviation as is shown in Figure 2.9. (Application of the central limit theorem to data whose underlying distribution is not normal often results in the valid use of the normal distribution.) When the number of data in the sample are large, the estimated (sample) standard deviation is approximately equal to the population standard deviation, and the following relationships are valid for the normally distributed variable:
- About 68.2% of the variable values are within ±s of mean.
- About 95.4% of the variable values are within ±2s of mean.
- About 99.7% of the variable values are within ±3s of mean.

In all control performance and beneﬁts analysis, the mean and standard deviation can be used in place of the frequency distribution when the distribution is normal. As is apparent, a narrow distribution is equivalent to a small standard deviation. Although the process data can often be characterized by a normal distribution, the method for calculating beneﬁts does not depend on the normal distribution, which was introduced here to relate the beneﬁts method to statistical terms often used to describe the variability of data.

The empirical histogram provides how often—that is, what percentage of the time—a variable has a certain value, with the value for each histogram entry taken as the center of the variable interval. The performance of plant operation at each variable value can be determined from the performance function. Depending on the plant, the performance function could be reactor conversion, efﬁciency, pro duction rate, proﬁt, or other variable that characterizes the quality of operation. The average performance for a set of representative data (that is, frequency distribution) is calculated by combining the histogram and proﬁt function according to the following equation (Bozenhardt and Dybeck, 1986; Marlin et al., 1991; and Stout and Cline, 1976).

>[!mathz]
>>[!eqn] Eqn 2.3
>>$$P_{ \mathrm{ave} } = \sum \limits _{j=1} ^{M} F_{j} P_{j}$$
>
>where 
>$$\begin{align}
P_{\text {ave }} &= \text{average process performance} \\
F_{j} &= \text{fraction of data in interval } j = N_{j}/N_{T} \\
N_{j} &= \text{number of data points in interval} j \\
N_{T} &= \text {total number of data points} \\
P_{j} &= \text {performance measured at the midpoint of interval } j \\
M &= \text{number of intervals in the frequency distribution}
\end{align}$$



#### 2.5 Importance of Control Engineering 
#### 2.6 Conclusions 
## Part 2: Process Dynamics
### Chapter 3: Mathematical Modelling Principles
#### 3.1 Introduction 
#### 3.2 A Modelling Procedure 
#### 3.3 Modelling Examples 
#### 3.4 Linearization 
#### 3.5 Numerical Solutions of Ordinary Differential Equations
#### 3.6 The Nonisothermal Chemical Reactor 
#### 3.7 Conclusions 
### Chapter 4: Modelling and Analysis for Process Control
#### 4.1 Introduction 
#### 4.2 The Laplace Transform 
#### 4.3 Input-Output Models and Transfer Functions
#### 4.4 Block Diagrams 
#### 4.5 Frequency Response 
#### 4.6 Conclusions 
### Chapter 5: Dynamic Behavior of Typical Process Systems
#### 5.1 Introduction 
#### 5.2 Basic System Elements 
#### 5.3 Series Structures of Simple Systems 
#### 5.4 Parallel Structures of Simple Systems 
#### 5.5 Recycle Structures 
#### 5.6 Staged Processes 
#### 5.7 Multiple Input-Multiple Output Systems
#### 5.8 Conclusions 
### Chapter 6: Empirical Model Identification
#### 6.1 Introduction 
#### 6.2 An Empirical Model Building Procedure 
#### 6.3 The Process Reaction Curve 
#### 6.4 Statistical Model Identification 
#### 6.5 Additional Topics in Identification 
#### 6.6 Conclusions 
## Part 3: Feedback Control
### Chapter 7: The Feedback Loop
#### 7.1 Introduction 
#### 7.2 Process and Instrument Elements of the Feedback Loop 
#### 7.3 Selecting Controlled and Manipulated Variables 
#### 7.4 Control Performance Measures for Common Input Changes 
#### 7.5 Approaches to Process Control 
#### 7.6 Conclusions 
### Chapter 8: The Proportional-Integral-Derivative (PID) Algorithm
### Chapter 9: PID Controller Tuning for Dynamic Performance
### Chapter 10: Stability Analysis and Controller Tuning Digital Implementation of Process Control
### Chapter 11: Digital Implementation of Process Control
### Chapter 12 Practical Application of Feedback Control
### Chapter 13 Performance of Feedback Control Systems
## Part 4: Enhancements to Single-Loop PID Feedback Control
### Chapter 14 Cascade Control
### Chapter 15 Feedforward Control
### Chapter 16 Adapting Single-Loop Control Systems for Nonlinear Processes
### Chapter 17 Inferential Control
### Chapter 18 Level and Inventory Control
### Chapter 19 Single-Variable Model Predictive Control
## Part 5: Multivariable Control
### Chapter 20: Multiloop Control - Effects of Interaction
### Chapter 21: Multiloop Control - Performance Analysis
### Chapter 22: Variable-Structure and Constraint Control
### Chapter 23: Centralized Multivariable Control
## Part 6: Process Control Design
### Chapter 24 Process Control Design - Definition and Decisions
### Chapter 25 Process Control Design - Managing the Design Procedure
### Chapter 26 Continual Improvement
## Appendices
### Appendix A Process Control Drawings
### Appendix B: Integrating Factor
### Appendix C: Chemical Reactor Modeling and Analysis
### Appendix D: Approximate Dynamic Models
### Appendix E: Determining Controller Contants to Satisfy
### Appendix F: Discrete Models for Digital Control
### Appendix G: Guide to Selected Process Examples
### Appendix H: Partial Fractions and Frequency Response
### Appendix I: Process Examples of Parallel Systems
### Appendix J: Process Control Case Study - Two Product Distillation
### Appendix K: Process Control Case Study - Fired Heater
### Appendix L: Analysis of Digital Control Systems
## Index