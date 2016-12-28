# Interview-Practice-Udacity
####   1. What’s your favorite tool or library for Android? Why is it so useful?
<p>     There are couple of libraries I really like, Picasso and Gson. Picasso is used in most of the apps, basically it is used to load the images from internet into a view. Picasso is based on okhhtp. Gson is useful in converting JSON into model classes. These classes can be further used to populate database or views. </p>
####   2. You want to open a map app from an app that you’re building. The address, city, state, and ZIP code are provided by the user. What steps are involved in sending that data to a map app?
<p> The information is sent through uri. So I would<br>
1. Get the full address, city, state from the user.
2. Then I will build a uri to pass it to the maps app.<br>
  String uri =  geo:0,0?q=my+street+address;
3. Then use the uri to create a Intent and Launch the maps activity</p>
####   3. Implement a method to perform basic string compression using the counts of repeated characters. For example, the string aabcccccaaa would become a2b1c5a3. If the "compressed" string would not become smaller than the original string, your method should return the original string. The method signature is: “public static String compress(String input)” You must write all code in proper Java, and please include import statements for any libraries you use.
```java    
    public static String compress(String input){
        int temp=1,i;
        String compressed= "";
        for(i=0;i<input.length() - 1 ; i++) {
            if (input.charAt(i) == input.charAt(i + 1))
                temp++;
            else{
                compressed = compressed + input.charAt(i) + temp;
                temp = 1;
            }
        }
        compressed = compressed + input.charAt(i) +  temp;
        return compressed.length()<input.length()?compressed:input;
    }
    public static void main(String[] args) {
            System.out.println(Main.compress("abcd"));
    }
```
####   4. List and explain the differences between four different options you have for saving data while making an Android app. Pick one, and explain (without code) how you would implement it..
<p>Database using content Provider, Shared Preferences, saving data in file and using online Api to store data like Firebase<br>To store data like name, email-id etc, Shared Prefrence can be used. Data is stored in a key-value form. So the saved data can be retrieved through key. To implement it first Editor is opened using edit(). Values are inserted using functions like putString(), putInt(). Then commit() is called to save those changes.</p>
####   5. What are your thoughts about Fragments? Do you like or hate them? Why?
<p> Fragments are useful in many cases, like when implementing slideable tabs, or sliding. Basically when we need to include multiple views into an activity. Another powerful feature of fragment is that it has its own Life Cycle. So in a way it acts as an sub-activity in a activity.
I kind of like it when I have to make complex layout with backstacks. For tablets they are quite useful for making mater flow type layouts</p>
####   6. If you were to start your Android position today, what would be your goals a year from now?
<p>My goals after one year would be to be to lead a team of android developers, and create an app that would be useful for masses. 
Also I would like to work for open source comunity and help people.</p>
