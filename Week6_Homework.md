## P.3.1
![image](https://github.com/Yankee1231/Control_engineering_summary/assets/138596644/f93c96b3-2f8e-4bc7-a493-174bffdb463b)
![image](https://github.com/Yankee1231/Control_engineering_summary/assets/138596644/668a35ea-5068-495d-b027-320358584191)

## P.3.3
![image](https://github.com/Yankee1231/Control_engineering_summary/assets/138596644/e12a8207-81d9-45a9-a91d-d26696093bee)
![image](https://github.com/Yankee1231/Control_engineering_summary/assets/138596644/d3f3076c-5000-4a97-b62b-3452762151be)

## P 3.5
![image](https://github.com/Yankee1231/Control_engineering_summary/assets/138596644/2a8e7c6f-abe8-448c-808e-12ea3bbe711c)

## P 3.12
![image](https://github.com/Yankee1231/Control_engineering_summary/assets/138596644/aff5241a-00ae-4ad7-ae42-cddc4a86adb7)
![image](https://github.com/Yankee1231/Control_engineering_summary/assets/138596644/5b431371-1df4-4d5f-a063-d8a1888ba7cc)

## P 3.17
![image](https://github.com/Yankee1231/Control_engineering_summary/assets/138596644/8910ae8c-c89a-4a51-9f39-992ce3ceae7b)

    % p3.1
    syms k b s
    A = [0 1; -k -b];
    B = [0; 1];
    C = [1 0];
    D = 0;
    Phi = inv(s*eye(2) - A);
    G = C*Phi*B + D;
    [n, d] = numden(G)

    num = flip(coeffs(n, s))
    den = flip(coeffs(d, s))

    [A, B, C, D] = tf2ss(num, den)


    % p3.12
    syms L C R s
    A = [0 1 0; 0 0 1; -48 -44 -12];
    B = [0; 0; 1];
    C = [40 8 0];
    D = 0;
    Phi = inv(s*eye(3) - A);
    G = C*Phi*B + D;
    [n, d] = numden(G)

    num = sym2poly(n)
    den = sym2poly(d)

    [A, B, C, D] = tf2ss(num, den)


     % p3.12
    syms L C R s
    A = [0 1 0; 0 0 1; -48 -44 -12];
    B = [0; 0; 1];
    C = [40 8 0];
    D = 0;
    Phi = inv(s*eye(3) - A);
    G = C*Phi*B + D;
    [n, d] = numden(G)

    num = sym2poly(n)
    den = sym2poly(d)

    [A, B, C, D] = tf2ss(num, den)


    Phi = ilaplace(inv(s*eye(3) - A))


    % p3.17
    A = [1 1 -1; 4 3 0; -2 1 10];
    B = [0; 0; 4]
    C = [1 0 0]
    D = 0;

    Phi = inv(s*eye(3) - A)
    G = C*Phi*B + D

'
