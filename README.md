# SwipeBackFragment
An Android library that can finish a Fragment / Activity with swipe-back gesture.

# Demo
<img src="gif/swipe.gif"/>

# How to use
1. Edit build.gradle
````java
implementation 'me.yokeyword:swipebackfragment:0.3.0'
````

2. Extends SwipeBackActivity / SwipeBackFragment
Activity Java:
````java
public class SampleActivity extends SwipeBackActivity {}
````

Activity Kotlin:
````java
class SampleActivity: SwipeBackActivity() {}
````

Fragment Java:
````java
public class SampleFragment extends SwipeBackFragment {
    @Override
    public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
        View view = inflater.inflate(R.layout.xxx, container, false);
        
        return attachToSwipeBack(view);
    }
}
````

Fragment Kotlin:
````java
class SampleFragment : SwipeBackFragment() {
    override fun onCreateView(inflater: LayoutInflater, container: ViewGroup, savedInstanceState: Bundle?): View {
        val view = inflater.inflate(R.layout.xxx, container, false)

        return attachToSwipeBack(view)
    }
}
````

3. Edit AppTheme in xml
````xml
 <item name="android:windowIsTranslucent">true</item>
````


4. Settings (Optional):
````java
  // Swipe EDGE (EDGE_LEFT(Default),EDGE_RIGHT,EDGE_TOP,EDGE_RIGHT,EDGE_ALL)
  getSwipeBackLayout().setEdgeOrientation(SwipeBackLayout.EDGE_RIGHT);
  
  // Disable Swipe Back
  getSwipeBackLayout().setEnableGesture(false);
  
  // Enable Swipe Back
  getSwipeBackLayout().setEnableGesture(true);
  
  // Swipe Listener
  getSwipeBackLayout().addSwipeListener();
````

# Credit
[ikew0ng/SwipeBackLayout](https://github.com/ikew0ng/SwipeBackLayout)
[YoKeyword/SwipeBackFragment](https://github.com/YoKeyword/SwipeBackFragment)

