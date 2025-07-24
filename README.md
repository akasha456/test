<pre> 
```mermaid
flowchart TD
    Start([Start])
    A[Step 1: Input Collection]
    A1[Collect PAN, Aadhaar, Employer Details]
    A2[Collect Income Details (Form 16, Bank, Freelance)]
    A3[Collect Deduction Proofs (80C, Rent, Loans)]
    A4[Collect Capital Gains Info]
    A5[Collect Special Status (HUF, Senior Citizen)]

    B[Step 2: Backend Processing]
    B1[Categorize Income and Deductions]
    B2[Select ITR Form via Decision Tree]
    B3[Compute Taxes under Both Regimes]
    B4[Suggest Best Regime]
    B5[Check for Errors]
    B6[Generate Checklist]

    C[Step 3: Output Generation]
    C1[Display Tax Summary and Compare Regimes]
    C2[Generate JSON (ITD schema)]
    C3[Generate PDF Report]
    C4[Optional Excel Sheet]

    D[Step 4: Submission Preparation]
    D1[Login via OTP/Token]
    D2[API Integration or Manual Upload]
    D3[Track Submission Status]

    End([End])

    Start --> A --> A1 --> A2 --> A3 --> A4 --> A5 --> B
    B --> B1 --> B2 --> B3 --> B4 --> B5 --> B6 --> C
    C --> C1 --> C2 --> C3 --> C4 --> D
    D --> D1 --> D2 --> D3 --> End

</pre>
