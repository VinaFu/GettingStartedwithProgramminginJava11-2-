# GettingStartedwithProgramminginJava11-2-
Plural Course

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
            // can be double[] new = {....}
            // double[] results = new double[opCodeas.length]
            // the number inside the last bracket indicates how many items.
    2) float new[0] 
        indicate each item
    
    
    
        package com.pluralsight.letsgetlogical;
        public class Main {
            public static void main(String[] args) {

                double[] leftVals = {100.0d, 25.0d, 225.0d, 11.0d};
                double[] rightVals = {50.0d, 92.d, 17.0d, 3.0d};
                char[] opCodes = {'d', 'a', 's', 'm'};
                double[] results = new double[opCodes.length];

                for(int i =0; i < opCodes.length; i++) {
                    switch (opCodes[i]) {
                        case 'a':
                            results[i] = leftVals[i] + rightVals[i];
                            break;
                        case 's':
                            results[i] = leftVals[i] - rightVals[i];
                            break;
                        case 'm':
                            results[i] = leftVals[i] * rightVals[i];
                            break;
                        case 'd':
                            results[i] = rightVals[i] != 0 ? leftVals[i] / rightVals[i] : 0.0d;
                            break;
                        default:
                            System.out.println("Invalid opCode: " + opCodes[i]);
                            results[i] = 0.0d;
                            break;
                    }
                }
                for(double currentResult : results)
                        // after for-loop, each item return current results
                    System.out.println(currentResult);
            }
        }
        
        
6. Understanding the methods -- calling/comments - terminal 

        double result = calculateInterest(100d, 0.05d, 10);
        System.out.println(result); // 50.0
        
        static double calculateInterest(double amt, double rate, int year){
            double interest = amt * rate * years;
            return interest;
        }               // you can call the calculatInternate first, define, then call. Before the call, you can have a " static"
                        // return a value


        comment - using terminal to exacute
        Tips: 1) use cd to get to the item you want;
              2) use "com.pluralsight.letsgetlogical.Main"  (from out-production till com) to execute in terminal
              3) executive in the terminal: Main a value1 value2


    So main is to launch all the processures and then define each function
    Pay attention to private static and public static when define a function
    Private static - can be access from the within the class only; public static - can be access both within and outside the class.
        
                package com.pluralsight.letsgetlogical;
                public class Main {
                    public static void main(String[] args) {

                        double[] leftVals = {100.0d, 25.0d, 225.0d, 11.0d};
                        double[] rightVals = {50.0d, 92.d, 17.0d, 3.0d};
                        char[] opCodes = {'d', 'a', 's', 'm'};
                        double[] results = new double[opCodes.length];

                        if(args.length == 0) {
                            for (int i = 0; i < opCodes.length; i++) {
                                results[i] = execute(opCodes[i], leftVals[i], rightVals[i]);
                            }
                            for (double currentResult : results)
                                System.out.println(currentResult);
                        }else if(args.length == 3)
                            handleCommandLine(args);
                        else
                            System.out.println("Please provide an operation code and 2 number values");
                    }
                    private static void handleCommandLine(String[] args){
                        char opCode = args[0].charAt(0);
                        double leftVal = Double.parseDouble(args[1]);
                        double rightVal = Double.parseDouble(args[2]);
                        double result = execute(opCode, leftVal, rightVal);
                        System.out.println(result);
                    }

                    static double execute(char opCode, double leftVal, double rightVal){
                        double result;
                        switch(opCode){
                            case 'a':
                                result = leftVal + rightVal;
                                break;
                            case 's':
                                result = leftVal - rightVal;
                                break;
                            case 'm':
                                result = leftVal * rightVal;
                                break;
                            case 'd':
                                result = rightVal != 0 ? leftVal / rightVal: 0.0d;
                                break;
                            default:
                                System.out.println("Invalid opCode: " + opCode);
                                result = 0.0d;
                                break;
                        }
                        return result;
                    }
                }

