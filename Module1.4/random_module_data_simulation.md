# Random Module + Data Simulation

     কেন দরকার?

     Machine Learning এ:

            random data লাগে
            train/test split লাগে
            simulation লাগে

             সবকিছু NumPy random দিয়ে করা হয়

     1. Random Number (0 থেকে 1)
                import numpy as np

                print(np.random.rand())

             Output: 0 থেকে 1 এর মধ্যে random float

             Multiple random number
                 print(np.random.rand(5))

             5টা random number

            Note:
                        কেন np.random.rand() লিখি?
                        কারণ Python-এ:
                        library → module → function এইভাবে access করতে হয়

                 ভিতরের structure (concept)
                    NumPy
                    └── random
                        └── rand()

                 মানে:
                    rand() = random module-এর function

     2. Random Integer
                print(np.random.randint(1, 10))

                 1 থেকে 9 এর মধ্যে random number

                 Multiple integer
                        print(np.random.randint(1, 100, size=5))

     3. Random Array (Matrix)
                arr = np.random.rand(2,3)
                print(arr)

                 2x3 matrix

     4. Choice (Random selection) 

                        data = [10, 20, 30, 40]
                        print(np.random.choice(data))

                random একটা value

                Multiple choice
                        print(np.random.choice(data, size=3))

     5. Seed (Same output বারবার পেতে) ⭐
                np.random.seed(1)

                print(np.random.rand(3))

                সবসময় same output দিবে

                    Note:
                         Seed =
                        "random number generator-এর starting point"

                 Real-life analogy 

                        ধরো:

                        তুমি dice খেলছো  → random result
                        কিন্তু যদি same way-এ same force দিয়ে ফেলো (seed fix) → same result আসবে

     6. Shuffle
            arr = np.array([1,2,3,4,5])

            np.random.shuffle(arr)
            print(arr)

             array mix হয়ে যাবে

                    Note
                         shuffle কী?

                         np.random.shuffle() হলো NumPy এর একটা function

                        কাজ:
                           array-এর element গুলোকে random ভাবে mix (shuffle) করে দেয়

     7. Distribution (Advanced - ML) 
            # normal distribution
                print(np.random.randn(5))

                mean = 0, std = 1

#      Note:
                what is normal distribution? → এইভাবে বললে আরও natural শোনাবে।

                Normal Distribution হলো এমন একটি distribution যেখানে বেশিরভাগ value mean-এর কাছাকাছি থাকে, আর খুব ছোট বা খুব বড় value কম থাকে।

                উদাহরণ:

                mean = average value
                std = standard deviation = data কতটা ছড়ানো

                যদি mean = 0 এবং std = 1 হয়, তাহলে একে Standard Normal Distribution বলে।

                μ=0, σ=1

                my code:
                        import numpy as np

                        print(np.random.randn(5))

                এখানে:

                randn() = random normal distribution থেকে number generate করে
                5 = 5টা random number generate হবে
                by default mean = 0 এবং std = 1

                Possible output:

                [ 0.25 -1.10  0.75  1.45 -0.30 ]

                এখানে numbers গুলো mostly 0-এর আশেপাশে থাকবে।

                আরও example:

                import numpy as np

                data = np.random.randn(5)

                print(data)
                print("Mean:", np.mean(data))
                print("Std:", np.std(data))

                যদি ami নিজের mean আর std দিতে chai:

                import numpy as np

                data = np.random.normal(loc=10, scale=2, size=5)

                print(data)

                এখানে:

                loc=10 → mean = 10
                scale=2 → std = 2
                size=5 → 5টা number

                মানে generated number গুলো mostly 10-এর আশেপাশে থাকবে, এবং spread হবে 2 অনুযায়ী।

     Mini Practice
                import numpy as np

                # random int
                print(np.random.randint(1,50, size=5))

                # random array
                arr = np.random.rand(3,3)
                print(arr)

                # shuffle
                np.random.shuffle(arr)
                print(arr)

     Real Life Use

            Dummy dataset তৈরি
            ML training/test split
            Data simulation

     Summary
                rand() → float random
                randint() → integer
                choice() → select
                seed() → fixed output
                shuffle() → mix
                randn() → normal distribution