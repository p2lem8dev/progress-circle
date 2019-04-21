# Progress Circle

This is a progress bar implemented as circle

#### Attributes

<table>
    <tr>
        <td>app:progress_bar_size</td>
        <td>Float</td>
    </tr><tr>
        <td>app:radius</td>
        <td>Float</td>
    </tr><tr>
        <td>android:progress</td>
        <td>Integer</td>
    </tr><tr>
        <td>android:background</td>
        <td>Color</td>
    </tr><tr>
        <td>app:primary_color</td>
        <td>Color</td>
    </tr><tr>
        <td>app:secondary_color</td>
        <td>Color</td>
    </tr><tr>
        <td>app:outline</td>
        <td>Boolean</td>
    </tr>
    <tr>
        <td>app:outline_color</td>
        <td>Color</td>
    </tr>
</table>

#### Events

<code>interface OnProgressChangeListener</code>
<br>
<code>onProgressChange(Float, Int)</code>

#### Properties

<table>
    <tr>
        <td>progress</td>
        <td>Float</td>
    </tr>
    <tr>
        <td>progressBarWidth</td>
        <td>Float</td>
    </tr>
    <tr>
        <td>progressChangeListener</td>
        <td>OnProgressChangeListener?</td>
    </tr>
    <tr>
        <td>radius</td>
        <td>Float</td>
    </tr>
    <tr>
        <td>isRenderOutlineCircle</td>
        <td>Boolean</td>
    </tr>
    <tr>
        <td>outlineColor</td>
        <td>Int</td>
    </tr>
    <tr>
        <td>primaryColor</td>
        <td>Int</td>
    </tr>
    <tr>
        <td>secondaryColor</td>
        <td>Int</td>
    </tr>
    <tr>
        <td>outlineColor</td>
        <td>Int</td>
    </tr>
    <tr>
        <td>duration</td>
        <td>Int</td>
    </tr><tr>
        <td>time</td>
        <td>Int</td>
    </tr>
</table>

#### Methods

<table>
    <tr>
        <td>reset(void)</td>
    </tr>
    <tr>
        <td>setCustomShader(Shader)</td>
    </tr>
    <tr>
        <td>translate(int)</td>
    </tr>
</table>

#### Example

<pre>
override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        
        val progressCircle: ProgressCircle = findViewById(R.id.progress_circular)
        progressCircle.progressChangeListener = this
        
        mediaPlayer = MediaPlayer()
        mediaPlayer.setDataSource("audio.mp3")
        progressCircle.duration = mediaPlayer.duration
    }

override fun onProgressChange(progress: Float, time: Int) {
    mediaPlayer.seekTo(time * 1000)
}
</pre>