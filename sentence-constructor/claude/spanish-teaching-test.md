<?xml version="1.0" encoding="UTF-8"?>
<spanish_teaching_system_tests>
    <metadata>
        <title>Spanish Teaching System Test Documentation</title>
        <version>1.0</version>
        <last_updated>2025-02-08</last_updated>
    </metadata>

    <test_categories>
        <state_transition_tests>
            <setup_state>
                <test id="ST001">
                    <input_type>english_sentence</input_type>
                    <expected_output>
                        <vocabulary_table>required</vocabulary_table>
                        <sentence_structure>required</sentence_structure>
                    </expected_output>
                    <validation_criteria>
                        <criterion>All essential vocabulary included</criterion>
                        <criterion>Structure matches difficulty level</criterion>
                    </validation_criteria>
                </test>
                
                <test id="ST002">
                    <input_type>complex_english_sentence</input_type>
                    <expected_output>
                        <component_breakdown>required</component_breakdown>
                        <beginner_level_structures>required</beginner_level_structures>
                    </expected_output>
                    <validation_criteria>
                        <criterion>Each component traceable to basic structures</criterion>
                    </validation_criteria>
                </test>
            </setup_state>

            <attempt_state>
                <test id="AT001">
                    <input_type>spanish_sentence_attempt</input_type>
                    <expected_output>
                        <feedback>constructive</feedback>
                        <interpretation>required</interpretation>
                    </expected_output>
                    <validation_criteria>
                        <criterion>Feedback points to specific improvements</criterion>
                        <criterion>Maintains positive reinforcement</criterion>
                    </validation_criteria>
                </test>
            </attempt_state>

            <clue_state>
                <test id="CL001">
                    <input_type>student_question</input_type>
                    <expected_output>
                        <clues>progressive</clues>
                        <hints>non_revealing</hints>
                    </expected_output>
                    <validation_criteria>
                        <criterion>Guides without providing direct answers</criterion>
                    </validation_criteria>
                </test>
            </clue_state>
        </state_transition_tests>

        <content_generation_tests>
            <vocabulary_table_tests>
                <test id="VT001">
                    <requirements>
                        <requirement>Include only nouns, verbs, adverbs, adjectives</requirement>
                        <requirement>No particles or conjugations</requirement>
                        <requirement>Dictionary forms only</requirement>
                    </requirements>
                    <validation_criteria>
                        <criterion>Consistent table format</criterion>
                        <criterion>Appropriate word forms</criterion>
                    </validation_criteria>
                </test>
            </vocabulary_table_tests>

            <sentence_structure_tests>
                <test id="SS001">
                    <requirements>
                        <requirement>Use generic placeholders</requirement>
                        <requirement>Avoid specific grammar markers</requirement>
                    </requirements>
                    <validation_criteria>
                        <criterion>Matches difficulty level</criterion>
                        <criterion>Uses standard placeholders</criterion>
                    </validation_criteria>
                </test>
            </sentence_structure_tests>
        </content_generation_tests>

        <test_data_sets>
            <basic_patterns>
                <pattern>
                    <english>The cat is black.</english>
                    <structure>[Subject] [Verb] [Adjective]</structure>
                    <expected_vocabulary>
                        <word type="noun">cat</word>
                        <word type="verb">to be</word>
                        <word type="adjective">black</word>
                    </expected_vocabulary>
                </pattern>
                <pattern>
                    <english>I eat breakfast every morning.</english>
                    <structure>[Subject] [Verb] [Object] [Time]</structure>
                    <expected_vocabulary>
                        <word type="verb">to eat</word>
                        <word type="noun">breakfast</word>
                        <word type="noun">morning</word>
                    </expected_vocabulary>
                </pattern>
            </basic_patterns>
        </test_data_sets>

        <evaluation_metrics>
            <metric id="VC">
                <name>Vocabulary Completeness</name>
                <scoring>
                    <score value="3">All necessary words included</score>
                    <score value="2">Missing non-essential words</score>
                    <score value="1">Missing essential words</score>
                </scoring>
            </metric>
            <metric id="SA">
                <name>Structure Appropriateness</name>
                <scoring>
                    <score value="3">Matches level perfectly</score>
                    <score value="2">Slightly complex</score>
                    <score value="1">Too complex/simple</score>
                </scoring>
            </metric>
        </evaluation_metrics>
    </test_categories>
</spanish_teaching_system_tests>