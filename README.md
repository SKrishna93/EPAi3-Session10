# Session 10 Assignment of EPAi3.0

## Sequence Types
__________________________________________________________________________________________________________________

### Question - 1

#### Objective: Create a Polygon Class where initializer takes in number of edges/vertices and circumradius. They have these properties edges, vertices, interior angle, edge length, apothem, area, perimeter. That has these functionalities, __repr__ function, implements equality (==) based on # vertices and circumradius (__eq__) and implements > based on number of vertices only (__gt__)

#### __regular_polygon__ :
+ This class is used to define regular polygons of 'n' sides and 'r' circum_radius
    
    ##### Attributes
    --------------
    * num_of_sides : int
        - Number of edges/vertices of a regular polygon
    * circum_radius : float
        - The circum radius of the regular polygo
    * interior_angle : float
        - Interior angle of the regular polygon
    * edge_length : float
        - Length of the sides of the regular polygon
    * apothem : float
        - The length of the perpendicular line drawn from the center of the polygon to one of its sides
    * area : float
        - The total area of the regular polygon
    * perimeter : float
        - The perimeter of the regular polygon
    
    ##### Methods
    --------------
    * __init__ (self, num_of_sides, circum_radius)
        - Used to initialize the regular_polygon objects
    * __repr__ (self)
        - Overwrites the default class object representations
    * __eq__ (self, other: object)
        - Checks the equality of the objects passed based on the number of vertices and circum radius
    * __gt__ (self, other: object)
        - Checks if one object is '>' than the other based on the number of vertices
__________________________________________________________________________________________________________________

### Question - 2

### Objective: Implement a Custom Polygon sequence type, where initializer takes in, number of vertices for largest polygon in the sequence and common circumradius for all polygons. That can provide these properties: max efficiency polygon: returns the Polygon with the highest area: perimeter ratio, that has these functionalities: functions as a sequence type (__getitem__), supports the len() function (__len__) and has a proper representation (__repr__) function

#### custom_polygon_sequence :
+ This class creates a sequence of polygon objects. It has the following attributes and methods

    ##### Attributes
    --------------
    largest_num_of_sides : int
        The polygon with largest number of sides in the sequence
    circum_rad : float
        The common circum radius of all the polygons in the sequence
    area_peri_ratios : dict()
        The dictionary to store the area and perimeter as values and vertices as keys

    ##### Methods
    -----------
    __init__ (largest_num_of_sides, circum_rad)
        This is a contructor for the custom_polygon_sequence class
    __getitem__ (vertex)
        This method implements getitem[index] for the sequence object
    __len__ ()
        This method implements in the len() function on the sequence object
    __repr__ ()
        This method overrides the default class object representation
    __max_efficiency_polygon__ ()
        This method computes the polygon with maximum area-perimeter ratio
    ___poly_ratio__ (int, circum_rad)
        This is a static method which computes the ratio between area and perimeter of each of the polygon