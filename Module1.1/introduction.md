# NumPy Introduction + Array Basics
    
     NumPy কি?

             NumPy = Numerical Python

             এটা দিয়ে আমরা:

                        Fast calculation করতে পারি
                        Array নিয়ে কাজ করতে পারি
                        ML এর math handle করতে পারি

     Install
                pip install numpy

     Import
                import numpy as np

#     1. Array কি?

     Array = list এর advanced version (fast + powerful)

     List vs NumPy Array
                            import numpy as np

                            # list
                            lst = [1, 2, 3, 4]

                            # numpy array
                            arr = np.array([1, 2, 3, 4])

                            print(arr)

     2. 1D Array
                    arr = np.array([10, 20, 30])
                    print(arr)

     3. 2D Array (Matrix) 
                            arr = np.array([
                                [1, 2, 3],
                                [4, 5, 6]
                            ])

                            print(arr)

                                  এটা table এর মতো (Pandas এর base)

     4. Array Properties
                            arr = np.array([[1,2,3],[4,5,6]])

                            print(arr.shape)   # (row, column)
                            print(arr.ndim)    # dimension
                            print(arr.size)    # total element
     5. Special Array
                     Zero array
                        np.zeros((2,3))

                     Ones array
                        .ones((2,2))

                     Range array
                        np.arange(0, 10)

#     Mini Practice
                    import numpy as np

                    arr = np.array([[1,2],[3,4]])

                    print(arr.shape)
                    print(arr.ndim)
                    print(arr.size)
    
#     Summary
                NumPy = fast math library
                Array = list এর powerful version
                1D, 2D array
                shape, size, dimension

# Note:

            List use করবে যখন:

                    Different type data রাখতে হবে
                    ছোট data হবে
                    শুধু basic store/use করতে হবে
                    Frequently add/remove করতে হবে

            Example:
                     student = ["Anwar", 21, True, 3.75]

            এখানে string, int, boolean, float একসাথে আছে। তাই list ভালো।

            আরও example:
                        numbers = [10, 20, 30]
                        numbers.append(40)
                        numbers.remove(20)

                    List flexible।

            Array use করবে যখন:

                    অনেক numeric data থাকবে
                    Fast calculation লাগবে
                    Machine Learning, Data Science, Math কাজ করবে
                    Element-wise operation লাগবে
                    Matrix / Table / Vector নিয়ে কাজ করবে

            Example:
                    import numpy as np

                    arr = np.array([10, 20, 30, 40])
                    print(arr * 2)

                    Output:

                    [20 40 60 80]

            List এ করলে:

                    lst = [10, 20, 30, 40]
                    print(lst * 2)

                    Output:

                    [10, 20, 30, 40, 10, 20, 30, 40]

            কারণ list multiplication repeat করে, কিন্তু array multiplication actual math operation করে।

            আরেকটা important difference:

            List:
                    a = [1, 2, 3]
                    b = [4, 5, 6]

                    print(a + b)

                    Output:

                    [1, 2, 3, 4, 5, 6]

            Array:
                    import numpy as np

                    a = np.array([1, 2, 3])
                    b = np.array([4, 5, 6])

                    print(a + b)

                    Output:

                    [5 7 9]

 *           সহজ rule:
                    সাধারণ Python data store = List
                    Math / ML / Data analysis = Array