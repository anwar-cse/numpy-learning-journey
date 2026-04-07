# Math Operations (NumPy Power)

     1. Basic Operations

                 NumPy array দিয়ে direct math করা যায়

                            import numpy as np

                            arr = np.array([1, 2, 3, 4])

                            print(arr + 10)   # [11 12 13 14]
                            print(arr * 2)    # [2 4 6 8]
                            print(arr - 1)    # [0 1 2 3]
                            print(arr / 2)    # [0.5 1 1.5 2]

                 প্রতিটা element এর উপর apply হয় (loop লাগে না)

     2. Array vs Array Operation
                a = np.array([1,2,3])
                b = np.array([4,5,6])

                print(a + b)   # [5 7 9]
                print(a * b)   # [4 10 18]

     3. Important Functions 
                arr = np.array([10, 20, 30, 40])

                print(arr.sum())   # total
                print(arr.mean())  # average
                print(arr.max())   # max
                print(arr.min())   # min

     4. Standard Deviation + Variance

                 ML এর জন্য খুব important

                print(arr.std())   # standard deviation
                print(arr.var())   # variance

     5. Square, Square Root
                print(np.sqrt(arr))   # root
                print(np.square(arr)) # square

     6. 2D Array Math
                arr = np.array([
                    [1,2,3],
                    [4,5,6]
                ])

                print(arr.sum())         # total
                print(arr.sum(axis=0))   # column wise
                print(arr.sum(axis=1))   # row wise

     7. Broadcasting  (Magic)
                arr = np.array([1,2,3])

                print(arr + 5)

                 Output:

                [6 7 8]

                 একটা value → পুরো array-এ apply হয়

     Mini Practice
                    import numpy as np

                    arr = np.array([2,4,6,8])

                    print(arr + 2)
                    print(arr.mean())
                    print(arr.max())
                    print(arr.std())

     Important Tips
                    NumPy loop ছাড়া fast calculation করে
                    ML এর সব calculation এখানে
                    Broadcasting খুব important

     Summary
                + - * / → element-wise
                sum(), mean(), max() → basic stats
                std(), var() → ML stats
                axis → row/column
                broadcasting → smart operation