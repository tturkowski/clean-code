# Task 4: Lack of Abstraction and Repetition

## Introduction
Welcome to Task 4! In this task, we'll be focusing on eliminating repetition and lack of abstraction. Repetitive code can lead to maintenance issues and inconsistencies, while abstraction can help simplify code and make it more reusable. We'll explore techniques to refactor the code to remove duplication and improve code quality.

## Hint

- Identify repeated patterns or structures in the code.
- Consider creating reusable abstractions to encapsulate common functionality.

## Code

```php
class ReportGenerator {
    public function generateSalesReport($salesData) {
        $report = '';
        foreach ($salesData as $data) {
            $report .= "Date: " . $data['date'] . "\n";
            $report .= "Product: " . $data['product'] . "\n";
            $report .= "Quantity: " . $data['quantity'] . "\n";
            $report .= "Price: $" . $data['price'] . "\n";
            $report .= "Total: $" . ($data['quantity'] * $data['price']) . "\n";
            $report .= "-------------------------\n";
        }
        return $report;
    }

    public function generateInventoryReport($inventoryData) {
        $report = '';
        foreach ($inventoryData as $data) {
            $report .= "Product: " . $data['product'] . "\n";
            $report .= "Stock: " . $data['stock'] . "\n";
            $report .= "Reorder Level: " . $data['reorder_level'] . "\n";
            $report .= "-------------------------\n";
        }
        return $report;
    }
}

$salesData = [
    ['date' => '2023-05-01', 'product' => 'Widget', 'quantity' => 4, 'price' => 19.99],
    ['date' => '2023-05-02', 'product' => 'Gadget', 'quantity' => 2, 'price' => 29.99],
];

$inventoryData = [
    ['product' => 'Widget', 'stock' => 50, 'reorder_level' => 10],
    ['product' => 'Gadget', 'stock' => 30, 'reorder_level' => 5],
];

$reportGenerator = new ReportGenerator();
echo $reportGenerator->generateSalesReport($salesData);
echo $reportGenerator->generateInventoryReport($inventoryData);
```
