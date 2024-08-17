import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class currencyconverter extends JFrame implements ActionListener {
    JComboBox<String> A7;
    JComboBox<String> A8;
    JTextField amountField;
    JLabel resultLabel;
    JButton convertButton;

    final double USD_TO_Indian_Rupee = 83.00;
    final double Indian_Rupee_TO_USD = 0.012;
    final double USD_TO_Canadian_Dollar = 1.34;
    final double Canadian_Dollar_TO_USD = 0.75;
    final double USD_TO_Chinese_Yuan = 7.30;
    final double Chinese_Yuan_TO_USD = 0.14;
    final double USD_TO_Japanese_Yen = 145.00;
    final double Japanese_Yen_TO_USD = 0.0069;
    final double USD_TO_British_Pound = 0.79;
    final double British_Pound_TO_USD = 1.26;

    currencyconverter() {
        setLayout(null);

        // Convert button
        convertButton = new JButton("CONVERT");
        convertButton.setBackground(Color.decode("#E8EAF6"));
        convertButton.setBounds(5, 410, 100, 35);
        convertButton.setFont(new Font("Arial", Font.ITALIC, 13));
        convertButton.addActionListener(this);
        add(convertButton);

        // Uppar vala panel
        JPanel A2 = new JPanel();
        A2.setBackground(Color.BLUE);
        A2.setBounds(0, 0, 500, 75);
        A2.setLayout(null);
        add(A2);

        // "TO" label
        JPanel A9 = new JPanel();
        A9.setBackground(Color.decode("#E8EAF6"));
        A9.setBounds(220, 190, 25, 25);
        add(A9);
        JLabel too = new JLabel("TO");
        A9.add(too);

        // Image
        ImageIcon i1 = new ImageIcon(ClassLoader.getSystemResource("Screenshot 2024-08-16 110419.png"));
        Image i2 = i1.getImage().getScaledInstance(80, 75, Image.SCALE_DEFAULT);
        ImageIcon i3 = new ImageIcon(i2);
        JLabel image = new JLabel(i3);
        image.setBounds(0, 0, 75, 75);
        A2.add(image);

//        Currency converter text
        JLabel cc = new JLabel("CURRENCY CONVERTER");
        cc.setBounds(155, 15, 400, 50);
        cc.setForeground(Color.YELLOW);
        cc.setFont(new Font("Arial", Font.BOLD, 18));
        A2.add(cc);

        // Amount Text
        JLabel J1 = new JLabel("ENTER THE AMOUNT: ");
        J1.setBounds(185, 60, 200, 50);
        J1.setFont(new Font("Arial", Font.ITALIC, 12));
        J1.setForeground(Color.BLACK);
        add(J1);

        // From currency label
        JLabel fromLabel = new JLabel("SELECT THE CURRENCY: ");
        fromLabel.setBounds(10, 150, 200, 35);
        fromLabel.setFont(new Font("Arial", Font.ITALIC, 12));
        fromLabel.setForeground(Color.BLACK);
        add(fromLabel);

        // To currency label
        JLabel toLabel = new JLabel("SELECT THE CURRENCY: ");
        toLabel.setBounds(310, 150, 230, 35);
        toLabel.setFont(new Font("Arial", Font.ITALIC, 12));
        toLabel.setForeground(Color.BLACK);
        add(toLabel);

        // Amount input field
        amountField = new JTextField();
        amountField.setBounds(209, 100, 75, 20);
        add(amountField);

        // Combo box 1
        String[] items = {"Indian_Rupee", "USD", "Canadian_Dollar", "Chinese_Yuan", "Japanese_Yen", "British_Pound"};
        A7 = new JComboBox<>(items);
        A7.setBounds(20, 190, 120, 20);
        A7.setBackground(Color.decode("#E8EAF6"));
        add(A7);

        // Combo box 2
        A8 = new JComboBox<>(items);
        A8.setBounds(325, 190, 120, 20);
        A8.setBackground(Color.decode("#E8EAF6"));
        add(A8);

        // Result label
        resultLabel = new JLabel("Result: ");
        resultLabel.setBounds(150, 414, 350, 25);
        resultLabel.setFont(new Font("Arial", Font.ITALIC, 18));
        resultLabel.setForeground(Color.WHITE);
        resultLabel.setForeground(Color.BLUE);
        add(resultLabel);

        // Frame
        setSize(500, 500);
        setLocation(500, 50);
        getContentPane().setBackground(Color.LIGHT_GRAY);
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        String from = (String) A7.getSelectedItem();
        String to = (String) A8.getSelectedItem();
        double amount = Double.parseDouble(amountField.getText());
        double convertedAmount = 0;

        // Conversion logic
        if (from.equals("USD") && to.equals("Indian_Rupee")) {
            convertedAmount = amount * USD_TO_Indian_Rupee;
        } else if (from.equals("Indian_Rupee") && to.equals("USD")) {
            convertedAmount = amount * Indian_Rupee_TO_USD;
        } else if (from.equals("USD") && to.equals("Canadian_Dollar")) {
            convertedAmount = amount * USD_TO_Canadian_Dollar;
        } else if (from.equals("Canadian_Dollar") && to.equals("USD")) {
            convertedAmount = amount * Canadian_Dollar_TO_USD;
        } else if (from.equals("USD") && to.equals("Chinese_Yuan")) {
            convertedAmount = amount * USD_TO_Chinese_Yuan;
        } else if (from.equals("Chinese_Yuan") && to.equals("USD")) {
            convertedAmount = amount * Chinese_Yuan_TO_USD;
        } else if (from.equals("USD") && to.equals("Japanese_Yen")) {
            convertedAmount = amount * USD_TO_Japanese_Yen;
        } else if (from.equals("Japanese_Yen") && to.equals("USD")) {
            convertedAmount = amount * Japanese_Yen_TO_USD;
        } else if (from.equals("USD") && to.equals("British_Pound")) {
            convertedAmount = amount * USD_TO_British_Pound;
        } else if (from.equals("British_Pound") && to.equals("USD")) {
            convertedAmount = amount * British_Pound_TO_USD;
        } else if (from.equals("Indian_Rupee") && to.equals("Canadian_Dollar")) {
            convertedAmount = amount * Indian_Rupee_TO_USD * USD_TO_Canadian_Dollar;
        } else if (from.equals("Canadian_Dollar") && to.equals("Indian_Rupee")) {
            convertedAmount = amount * Canadian_Dollar_TO_USD * USD_TO_Indian_Rupee;
        } else if (from.equals("Indian_Rupee") && to.equals("Chinese_Yuan")) {
            convertedAmount = amount * Indian_Rupee_TO_USD * USD_TO_Chinese_Yuan;
        } else if (from.equals("Chinese_Yuan") && to.equals("Indian_Rupee")) {
            convertedAmount = amount * Chinese_Yuan_TO_USD * USD_TO_Indian_Rupee;
        } else if (from.equals("Indian_Rupee") && to.equals("Japanese_Yen")) {
            convertedAmount = amount * Indian_Rupee_TO_USD * USD_TO_Japanese_Yen;
        } else if (from.equals("Japanese_Yen") && to.equals("Indian_Rupee")) {
            convertedAmount = amount * Japanese_Yen_TO_USD * USD_TO_Indian_Rupee;
        } else if (from.equals("Indian_Rupee") && to.equals("British_Pound")) {
            convertedAmount = amount * Indian_Rupee_TO_USD * USD_TO_British_Pound;
        } else if (from.equals("British_Pound") && to.equals("Indian_Rupee")) {
            convertedAmount = amount * British_Pound_TO_USD * USD_TO_Indian_Rupee;
        } else if (from.equals("Canadian_Dollar") && to.equals("Chinese_Yuan")) {
            convertedAmount = amount * Canadian_Dollar_TO_USD * USD_TO_Chinese_Yuan;
        } else if (from.equals("Chinese_Yuan") && to.equals("Canadian_Dollar")) {
            convertedAmount = amount * Chinese_Yuan_TO_USD * USD_TO_Canadian_Dollar;
        } else if (from.equals("Canadian_Dollar") && to.equals("Japanese_Yen")) {
            convertedAmount = amount * Canadian_Dollar_TO_USD * USD_TO_Japanese_Yen;
        } else if (from.equals("Japanese_Yen") && to.equals("Canadian_Dollar")) {
            convertedAmount = amount * Japanese_Yen_TO_USD * USD_TO_Canadian_Dollar;
        } else if (from.equals("Canadian_Dollar") && to.equals("British_Pound")) {
            convertedAmount = amount * Canadian_Dollar_TO_USD * USD_TO_British_Pound;
        } else if (from.equals("British_Pound") && to.equals("Canadian_Dollar")) {
            convertedAmount = amount * British_Pound_TO_USD * USD_TO_Canadian_Dollar;
        } else if (from.equals("Chinese_Yuan") && to.equals("Japanese_Yen")) {
            convertedAmount = amount * Chinese_Yuan_TO_USD * USD_TO_Japanese_Yen;
        } else if (from.equals("Japanese_Yen") && to.equals("Chinese_Yuan")) {
            convertedAmount = amount * Japanese_Yen_TO_USD * USD_TO_Chinese_Yuan;
        } else if (from.equals("Chinese_Yuan") && to.equals("British_Pound")) {
            convertedAmount = amount * Chinese_Yuan_TO_USD * USD_TO_British_Pound;
        } else if (from.equals("British_Pound") && to.equals("Chinese_Yuan")) {
            convertedAmount = amount * British_Pound_TO_USD * USD_TO_Chinese_Yuan;
        } else if (from.equals("Japanese_Yen") && to.equals("British_Pound")) {
            convertedAmount = amount * Japanese_Yen_TO_USD * USD_TO_British_Pound;
        } else if (from.equals("British_Pound") && to.equals("Japanese_Yen")) {
            convertedAmount = amount * British_Pound_TO_USD * USD_TO_Japanese_Yen;
        } else {
            convertedAmount = amount;
        }

//        result
        resultLabel.setText("Result :    " + String.format("%.2f", convertedAmount) + "  " + to);

    }

    public static void main(String[] args) {
        new currencyconverter();
    }
}
