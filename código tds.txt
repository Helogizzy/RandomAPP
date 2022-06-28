package com.example.sorteadorzinho;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.Button;
import android.widget.TextView;
import android.view.View;
import java.util.Random;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Button botao = findViewById(R.id.button);

        botao.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                randonNumero(view);
            }
        });
    }

    public void randonNumero(View view) {
        TextView textoResultado = findViewById(R.id.TextoResultado);
        int numero = new Random().nextInt(11);
        textoResultado.setText("O número selecionado é: " + numero);
    }
}