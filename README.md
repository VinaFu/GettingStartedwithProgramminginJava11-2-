# GettingStartedwithProgramminginJava11-2-

Section Two (Start with unit 5)

5. Looping & Arrays

    while -  repeat once qualify
    do {..} while (condition) - run at least once
    for --- you know how many times u need to loop
            for (initialize; condition; update)
            statement

    float[] theVals = new float[3];
    theVals[0] = 10.0f;
    theVals[1] = 20.0f;
    theVals[2] = 15.0f;
         //float theVals = {10.0f, 20.0f, 15.0f}; also works
    float sum = 0.0f;
    for(int index = 0; index < theVals.length; index++)
        sum += theVals[index];
    System.out.println(sum);
        // different with Python, index++  ||  range(len()):

    Array: 
    1) float[] name = {item, items, itemss};
        can be double[] new = {....}
    2) float new[0] 
        indicate each item
        

