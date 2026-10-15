
package com.gharchakirana.app;

import android.app.Activity;
import android.os.Bundle;
import android.content.Intent;
import android.net.Uri;

public class MainActivity extends Activity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);

        Intent intent = new Intent(
            Intent.ACTION_VIEW,
            Uri.parse("https://gharacha-kiraana.web.app")
        );

        intent.addCategory(Intent.CATEGORY_BROWSABLE);
        startActivity(intent);
        finish();
    }
}
