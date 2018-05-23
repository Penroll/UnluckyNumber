# UnluckyNumber
For CP2 in C#

        int[] array = new int[] {1, 2, 3, 4, 5, 6};
        List<int> iList = new List<int>();
        int Index;
        
        public Form1()
        {
            InitializeComponent();
            iList.AddRange(array);
            for (int i = 0; i < iList.Count; i++)
            {
                lblOutput.Text += iList[i] + ", ";
            }
        }

        private void btnRemove_Click(object sender, EventArgs e)
        {
            lblOutput.Text = "";
            int RemovedNumber = Convert.ToInt32(txtInput.Text);
            Index = iList.IndexOf(RemovedNumber);
            iList.Remove(RemovedNumber);
            for (int i = 0; i < iList.Count; i++)
            {
                    lblOutput.Text += iList[i] + ", ";
            }
            
        }

        private void btnReplace_Click(object sender, EventArgs e)
        {
            lblOutput.Text = "";
            int ReplacedAddition = Convert.ToInt32(txtReplacement.Text);
            iList.Insert(Index, ReplacedAddition);
            for (int i = 0; i < iList.Count; i++)
            {
                lblOutput.Text += iList[i] + ", ";
            }
