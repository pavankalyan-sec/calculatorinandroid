## EX:NO:05:Develop a program to create a simple calculator using android studio.
## Aim:
To create and design an android application for a simple calculator using android studio.
## EQUIPMENTS REQUIRED:
Android Studio(Latest Version)
## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as smsintent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6:Display details give in MainActivity file.

Step 7: Save and run the application.
## PROGRAM:
Program to create and design an android application simple calculator using Intent.
### Developed by: Pavan Kalyan P
### Registeration Number : 212225240104

### activity_main.xml
```
        <?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@color/calc_background"
    android:orientation="vertical"
    android:padding="16dp"
    tools:context=".MainActivity">

    <!-- Display Card Area -->
    <com.google.android.material.card.MaterialCardView
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1"
        android:layout_marginBottom="16dp"
        app:cardBackgroundColor="@color/calc_display_bg"
        app:cardCornerRadius="24dp"
        app:cardElevation="2dp"
        app:strokeWidth="0dp">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:gravity="bottom|end"
            android:orientation="vertical"
            android:padding="20dp">

            <!-- Expression Display -->

            <TextView
                android:id="@+id/textView"
                android:layout_width="326dp"
                android:layout_height="wrap_content"
                android:text="EXP-05 SIMPLE CALCULATOR"
                android:textAlignment="center"
                android:textSize="16sp"
                android:textStyle="bold" />

            <TextView
                android:id="@+id/tvExpression"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:gravity="end"
                android:maxLines="2"
                android:textColor="@color/text_expression"
                android:textSize="24sp"
                tools:text="125 + 45" />

            <!-- Result Display -->
            <TextView
                android:id="@+id/tvResult"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:layout_marginTop="8dp"
                android:gravity="end"
                android:maxLines="1"
                android:text="@string/default_result"
                android:textColor="@color/text_result"
                android:textSize="44sp"
                android:textStyle="bold"
                tools:text="170" />


        </LinearLayout>
    </com.google.android.material.card.MaterialCardView>

    <!-- Keypad Grid Area -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:layout_weight="1.8"
        android:orientation="vertical">

        <!-- Row 1: C, DEL, %, ÷ -->
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:orientation="horizontal">

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btnClear"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="@string/btn_clear"
                android:textColor="@color/btn_action_text"
                android:textSize="20sp"
                android:textStyle="bold"
                app:backgroundTint="@color/btn_action_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btnDelete"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="@string/btn_delete"
                android:textColor="@color/btn_action_text"
                android:textSize="18sp"
                android:textStyle="bold"
                app:backgroundTint="@color/btn_action_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btnModulo"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="@string/btn_modulo"
                android:textColor="@color/btn_op_text"
                android:textSize="22sp"
                android:textStyle="bold"
                app:backgroundTint="@color/btn_op_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btnDivide"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="@string/btn_divide"
                android:textColor="@color/btn_op_text"
                android:textSize="24sp"
                android:textStyle="bold"
                app:backgroundTint="@color/btn_op_bg"
                app:cornerRadius="20dp" />
        </LinearLayout>

        <!-- Row 2: 7, 8, 9, × -->
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:orientation="horizontal">

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn7"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="7"
                android:textColor="@color/btn_digit_text"
                android:textSize="22sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn8"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="8"
                android:textColor="@color/btn_digit_text"
                android:textSize="22sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn9"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="9"
                android:textColor="@color/btn_digit_text"
                android:textSize="22sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btnMultiply"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="@string/btn_multiply"
                android:textColor="@color/btn_op_text"
                android:textSize="24sp"
                android:textStyle="bold"
                app:backgroundTint="@color/btn_op_bg"
                app:cornerRadius="20dp" />
        </LinearLayout>

        <!-- Row 3: 4, 5, 6, − -->
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:orientation="horizontal">

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn4"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="4"
                android:textColor="@color/btn_digit_text"
                android:textSize="22sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn5"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="5"
                android:textColor="@color/btn_digit_text"
                android:textSize="22sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn6"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="6"
                android:textColor="@color/btn_digit_text"
                android:textSize="22sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btnSubtract"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="@string/btn_subtract"
                android:textColor="@color/btn_op_text"
                android:textSize="24sp"
                android:textStyle="bold"
                app:backgroundTint="@color/btn_op_bg"
                app:cornerRadius="20dp" />
        </LinearLayout>

        <!-- Row 4: 1, 2, 3, + -->
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:orientation="horizontal">

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn1"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="1"
                android:textColor="@color/btn_digit_text"
                android:textSize="22sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn2"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="2"
                android:textColor="@color/btn_digit_text"
                android:textSize="22sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn3"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="3"
                android:textColor="@color/btn_digit_text"
                android:textSize="22sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btnAdd"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="@string/btn_add"
                android:textColor="@color/btn_op_text"
                android:textSize="24sp"
                android:textStyle="bold"
                app:backgroundTint="@color/btn_op_bg"
                app:cornerRadius="20dp" />
        </LinearLayout>

        <!-- Row 5: 00, 0, ., = -->
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="0dp"
            android:layout_weight="1"
            android:orientation="horizontal">

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn00"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="@string/btn_00"
                android:textColor="@color/btn_digit_text"
                android:textSize="20sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btn0"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="0"
                android:textColor="@color/btn_digit_text"
                android:textSize="22sp"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btnDot"
                style="@style/Widget.Material3.Button.TonalButton"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="@string/btn_dot"
                android:textColor="@color/btn_digit_text"
                android:textSize="24sp"
                android:textStyle="bold"
                app:backgroundTint="@color/btn_digit_bg"
                app:cornerRadius="20dp" />

            <com.google.android.material.button.MaterialButton
                android:id="@+id/btnEquals"
                style="@style/Widget.Material3.Button"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_margin="4dp"
                android:layout_weight="1"
                android:text="@string/btn_equals"
                android:textColor="@color/btn_equal_text"
                android:textSize="26sp"
                android:textStyle="bold"
                app:backgroundTint="@color/btn_equal_bg"
                app:cornerRadius="20dp" />
        </LinearLayout>

    </LinearLayout>

</LinearLayout>

```

MainActivity.java

```
package com.example.exp_5_simple_calculator;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    private TextView tvExpression;
    private TextView tvResult;

    private final StringBuilder currentExpression = new StringBuilder();
    private boolean isResultCalculated = false;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);

        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) -> {
            Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
            return insets;
        });

        initViews();
        setupListeners();
    }

    private void initViews() {
        tvExpression = findViewById(R.id.tvExpression);
        tvResult = findViewById(R.id.tvResult);
    }

    private void setupListeners() {
        // Digit Buttons
        int[] digitButtonIds = {
                R.id.btn0, R.id.btn1, R.id.btn2, R.id.btn3, R.id.btn4,
                R.id.btn5, R.id.btn6, R.id.btn7, R.id.btn8, R.id.btn9, R.id.btn00
        };

        View.OnClickListener digitListener = v -> {
            Button button = (Button) v;
            appendDigit(button.getText().toString());
        };

        for (int id : digitButtonIds) {
            findViewById(id).setOnClickListener(digitListener);
        }

        // Decimal Point
        findViewById(R.id.btnDot).setOnClickListener(v -> appendDot());

        // Operator Buttons
        int[] operatorButtonIds = {
                R.id.btnAdd, R.id.btnSubtract, R.id.btnMultiply, R.id.btnDivide, R.id.btnModulo
        };

        View.OnClickListener operatorListener = v -> {
            Button button = (Button) v;
            appendOperator(button.getText().toString());
        };

        for (int id : operatorButtonIds) {
            findViewById(id).setOnClickListener(operatorListener);
        }

        // Action Buttons
        findViewById(R.id.btnClear).setOnClickListener(v -> clearAll());
        findViewById(R.id.btnDelete).setOnClickListener(v -> deleteLastChar());
        findViewById(R.id.btnEquals).setOnClickListener(v -> calculateResult());
    }

    private void appendDigit(String digit) {
        if (isResultCalculated) {
            currentExpression.setLength(0);
            isResultCalculated = false;
        }

        currentExpression.append(digit);
        updateDisplay();
        tryAutoCalculate();
    }

    private void appendDot() {
        if (isResultCalculated) {
            currentExpression.setLength(0);
            isResultCalculated = false;
        }

        if (currentExpression.length() == 0) {
            currentExpression.append("0.");
        } else {
            String expr = currentExpression.toString();
            int lastOpIndex = getLastOperatorIndex(expr);
            String currentToken = lastOpIndex == -1 ? expr : expr.substring(lastOpIndex + 1);

            if (!currentToken.contains(".")) {
                currentExpression.append(".");
            }
        }
        updateDisplay();
    }

    private void appendOperator(String op) {
        if (isResultCalculated) {
            String prevResult = tvResult.getText().toString();
            if (!prevResult.equals("0") && !prevResult.equals("Error")) {
                currentExpression.setLength(0);
                currentExpression.append(prevResult);
            }
            isResultCalculated = false;
        }

        if (currentExpression.length() == 0) {
            if (op.equals("−")) {
                currentExpression.append(op);
                updateDisplay();
            }
            return;
        }

        char lastChar = currentExpression.charAt(currentExpression.length() - 1);
        if (isOperatorChar(lastChar)) {
            currentExpression.setCharAt(currentExpression.length() - 1, op.charAt(0));
        } else {
            currentExpression.append(op);
        }

        updateDisplay();
    }

    private void clearAll() {
        currentExpression.setLength(0);
        isResultCalculated = false;
        tvExpression.setText("");
        tvResult.setText(R.string.default_result);
    }

    private void deleteLastChar() {
        if (isResultCalculated) {
            clearAll();
            return;
        }

        if (currentExpression.length() > 0) {
            currentExpression.deleteCharAt(currentExpression.length() - 1);
            updateDisplay();
            tryAutoCalculate();
        }
    }

    private void calculateResult() {
        if (currentExpression.length() == 0) {
            return;
        }

        try {
            String result = CalculatorEvaluator.evaluate(currentExpression.toString());
            tvResult.setText(result);
            isResultCalculated = true;
        } catch (ArithmeticException e) {
            tvResult.setText(R.string.error_division_by_zero);
            isResultCalculated = true;
        } catch (Exception e) {
            tvResult.setText(R.string.error_invalid_format);
            isResultCalculated = true;
        }
    }

    private void tryAutoCalculate() {
        if (currentExpression.length() == 0) {
            tvResult.setText(R.string.default_result);
            return;
        }

        char lastChar = currentExpression.charAt(currentExpression.length() - 1);
        if (isOperatorChar(lastChar)) {
            return;
        }

        try {
            String result = CalculatorEvaluator.evaluate(currentExpression.toString());
            tvResult.setText(result);
        } catch (Exception ignored) {
            // Ignore incomplete formulas during live typing preview
        }
    }

    private void updateDisplay() {
        tvExpression.setText(currentExpression.toString());
        if (currentExpression.length() == 0) {
            tvResult.setText(R.string.default_result);
        }
    }

    private boolean isOperatorChar(char c) {
        return c == '+' || c == '−' || c == '×' || c == '÷' || c == '%';
    }

    private int getLastOperatorIndex(String expr) {
        for (int i = expr.length() - 1; i >= 0; i--) {
            if (isOperatorChar(expr.charAt(i))) {
                return i;
            }
        }
        return -1;
    }
}

```

## Output:
<img width="1917" height="1072" alt="image" src="https://github.com/user-attachments/assets/8b547b2f-c615-4104-b77f-2ed2edcdf5e0" />
<img width="1917" height="1078" alt="image" src="https://github.com/user-attachments/assets/da6347a5-bd24-4682-8502-b19b008e8202" />




## RESULT
Thus a Simple Android Application create a simple calculator using Android Studio is developed and executed successfully.
