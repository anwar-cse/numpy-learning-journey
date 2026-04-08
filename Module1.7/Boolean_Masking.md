# Concept: Condition দিয়ে array filter করা

        Basic Example
            import numpy as np

            arr = np.array([10, 20, 30, 40, 50])

            mask = arr > 25
            print(mask)

        Output:
             [False False  True  True  True]

        Filtering Data
              print(arr[arr > 25])

        Output:
              [30 40 50]

#        Multiple Condition
             print(arr[(arr > 20) & (arr < 50)])

        Output:
             [30 40]

        OR Condition
             print(arr[(arr < 20) | (arr > 40)])

        Modify using condition 
             arr[arr > 30] = 100
             print(arr)

        Output:
            [10 20 30 100 100]

        2D Example
                arr = np.array([
                    [10,20,30],
                    [40,50,60]
                ])

                print(arr[arr > 30])

        Output:
            [40 50 60]

*        Mini Practice
                    import numpy as np

                    arr = np.array([5, 10, 15, 20, 25])

                    # 1. > 10 filter
                    # 2. even numbers বের করো
                    # 3. 20 এর বেশি value 0 করে দাও

*        Real Life Use
                Data cleaning
                Outlier remove
                ML preprocessing
                Filtering dataset
*        Summary
                condition → True/False array
                arr[condition] → filter
                &, | → multiple condition
                modify possible