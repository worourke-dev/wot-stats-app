<script lang="ts">
    import Button from '@smui/button';
    import Textfield from '@smui/textfield';
    import Icon from '@smui/textfield/icon';
    import HelperText from '@smui/textfield/helper-text';
    import Select, { Option } from '@smui/select';
    import LayoutGrid, { Cell } from '@smui/layout-grid';

    let valueA = '';
    let regions = ['NA Server', 'EU Server', 'Russian Server', 'SEA Server'];
    let selectedRegion = 'NA Server';
</script>

<LayoutGrid
  align="middle"
  fixedColumnWidth
>
    <Cell span={4}>
        <div>
            <Textfield variant="outlined" bind:value={valueA} label="Tanker name">
            </Textfield>
        </div>
    </Cell>
    <Cell span={4}>
        <div>
            <Select variant="outlined" bind:value={selectedRegion} label="Region">
                {#each regions as region}
                    <Option value={region}>{region}</Option>
                {/each}
            </Select>
        </div>
    </Cell>
    <Cell span={4}>
        <div>
            <Button variant="raised">Show Stats</Button>
        </div>
    </Cell>
</LayoutGrid>