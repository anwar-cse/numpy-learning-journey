# NaN / Missing Data Handling
        NaN কী?

         NaN = Not a Number
         Missing / invalid data represent করতে use হয়

         Example
            import numpy as np

            arr = np.array([10, 20, np.nan, 40])

            print(arr)

         Output:
             [10. 20. nan 40.]

         Problem
                Normal function use করলে problem হয়

                    print(arr.mean())

                Output:
                        nan

            কারণ NaN থাকলে পুরো result NaN হয়ে যায়

     Solution: NaN-safe Functions 
        print(np.nanmean(arr))  # mean ignore NaN
        print(np.nansum(arr))   # sum ignore NaN
        print(np.nanmax(arr))   # max ignore NaN
        print(np.nanmin(arr))   # min ignore NaN

     Check NaN
        print(np.isnan(arr))

        Output:
            [False False  True False]
 
        Remove NaN
            clean = arr[~np.isnan(arr)]
            print(clean)

         Output:
             [10. 20. 40.]

        
        Replace NaN 
        1. Replace with fixed value
                arr[np.isnan(arr)] = 0
                print(arr)
        2. Replace with mean (ML friendly)
                arr = np.array([10, 20, np.nan, 40])

                mean = np.nanmean(arr)
                arr[np.isnan(arr)] = mean

                print(arr)

             Output:
                 [10. 20. 23.33 40.]

         2D Example
                arr = np.array([
                    [10, np.nan, 30],
                    [40, 50, np.nan]
                ])

                print(np.nanmean(arr, axis=0))  # column-wise

        Important Note

            NaN শুধু float type-এ থাকে
            int array-এ NaN রাখা যায় না

         Mini Practice
                import numpy as np

                arr = np.array([5, np.nan, 15, np.nan, 25])

                # 1. NaN detect করো
                # 2. NaN remove করো
                # 3. mean দিয়ে replace করো

        Real Life Use
                Dataset cleaning
                Missing value handling
                ML preprocessing
                Data imputation

         Summary
                NaN = missing data
                mean() ❌ → nan
                nanmean() ✅
                isnan() → detect
                replace / remove possible